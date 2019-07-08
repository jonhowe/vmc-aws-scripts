# vmc-aws-scripts

VMware Cloud on AWS Scripts

## Overview

The scripts contained in this repository interact with the VMware Cloud on AWS REST API. As such, they read a text file named **.vmc-aws-auth.txt** in your home directory. The files should be well-documented with comments so be sure to review them before running.

 *(**NOTE:** If you run one of the scripts and the file is not found, you will be prompted for the necessary information and the file will be created for you!)*

 For reference, the contents of that config file are as follows:

```bash
# Organization Name: Your Organization Name here
export ORGID="your-organization-id-here"
export REFRESH_TOKEN="your-refresh-token-here"
```

## org

Organization level scripts:

- /org/get-vmc-org-json.sh : Retrieves details for the specified organization and outputs them into ORG_INFO.json

## sddc

- /sddc/get-vmc-sddcs-json.sh : Gets details on all SDDCs created in the specified organization and outputs them into SDDCS_INFO.json
- /sddc/show-sddcs-info.sh : this script will process and display a summary from the SDDCS_INFO.json file generated by the /sddc/get-vmc-sddcs-json.sh script
- /sddc/get-vmc-sddc-info.sh : Displays a summary for the given SDDC, and outputs the info to SDDC_INFO.json
- /sddc/create-vmc-sddc.sh : Creates 1 or more SDDCs using the specified parameters or safe defaults. Note that if a provider is not specified or is not typed correctly, then ZEROCLOUD will be used by default so that no charges result from an accidentally deployed SDDC.
