# SD-WAN Version Leakage

## Overview
The most popular and known SD-WAN solutions are enumerated using search engines.

## Vendors
- [VMWare NSX SD-WAN](#vmware-nsx-sd-wan)
- [TELoIP VINO SD-WAN](#teloip-vino-sd-wan)
- [Fatpipe SYMPHONY SD-WAN](#fatpipe-symphony-sd-wan)
- [Cisco Viptela SD-WAN](#cisco-viptela-sd-wan)
- [Versa Networks](#versa-networks)
- [Riverbed SD-WAN](#riverbed-sd-wan)
- [Citrix NetScaler SD-WAN](#citrix-netscaler-sd-wan)
- [Silver Peak SD-WAN](#silver-peak-sd-wan)
- [Talari SD-WAN](#talari-sd-wan)
- [Sonus SD-WAN](#sonus-sd-wan)
- [Arista Networks EOS](#arista-networks-eos)
- [Glue Networks](#glue-networks)

## VMWare NSX SD-WAN
### VeloCloud Network Orchestrator
Dislosure: UI info  
Source: HTTP response  
Example:
```
<link href="/css/vco-ui.3.0.0.1509625568730.common.css" rel="stylesheet">
```

## TELoIP VINO SD-WAN
### Teloip Orchestrator API
Dislosure: API version  
Source: HTML  
Example:
```
{"usage":"append '?debug=requestinfo' to any querystring. Optional params: virtualPathCount",
"host":"_v5.02_Teloip Orchestrator API","hostType":"SelfHost (AppHostBase)",...}
```

## Fatpipe SYMPHONY SD-WAN
### WARP
Dislosure: product version  
Source: HTML  
Example:
```
<h2 style="margin-top:5px;">FatPipe WARP</h2>
    <h5>9.1.2r142</h5>
```

## Cisco Viptela SD-WAN
### Cisco vEdge
Dislosure: product version  
Source: SSH MOTD  
Example:
```
viptela 17.2.4
```

### Cisco vBond
Dislosure: product version  
Source: SSH MOTD  
Example:
```
viptela 17.2.4
```


## Versa Networks
### Versa Analytics
Dislosure: Analytics version  
Source: JavaScript (`/versa/app/js/common/constants.js`)  
Example:
```
ANALYTICS_PATH : "/analytics/v1.0.0/",
REPORTING_PATH : "/analytics/v1.0.0/",
CLEANUP_PATH : "/analytics/v0.0.1/",
...
```

### Versa FlexVNF
Dislosure: product version  
Source: JavaScript (`scripts/main-layout/main-layout-controller.js`)  
Example:
```
{
    "collection": {
        "system:package-info": [
            {
                "package-id": "494bf5c",
                "major": 16,
                "minor": 1,
                "date": "20161214",
                "package-name": "versa-flexvnf-20161214-191033-494bf5c-16.1R2",
                "reltype": "R2",
                "build_type": "beta",
                "branch": "16.1R2",
                "creator": "manju"
            }
        ]
    }
}
```


## Riverbed SD-WAN
### Riverbed SteelHead
Dislosure: indirect version  
Source: HTML  
Example:
```
<meta name="application-name" content="web3 v0.15.8" />
```

## Citrix NetScaler SD-WAN
### Citrix NetScaler SD-WAN VPX
Dislosure: product version  
Source: HTML  
Example 1:
```
<link href="/br_ui/rdx/core/css/rdx.css?v=9.3.1.35" rel="stylesheet" type="text/css"/> 
<link href="/br_ui/app/css/br.css?v=9.3.1.35" rel="stylesheet" type="text/css"/> 
```

Example 2:
```
<meta http-equiv="Content-type" content="text/html; charset=utf-8" />
			<title>DC | Login</title>
			<link href="/vw/css/vw.css?R9_2_0_147_583054" rel="stylesheet" type="text/css" />

```

Example 3:
```
<meta http-equiv="Content-type" content="text/html; charset=utf-8" />
			<title> | Login</title>
			<link href="/vw/css/vw.css?R10_0_2_37_686956" rel="stylesheet" type="text/css" />

```

## Silver Peak SD-WAN
### Silver Peak Unity Orchestrator
Dislosure: product version  
Source: URL  
Example:
```
https://example.com/https:/8.1.4.11_66255/php/user_login.php
```

### Silver Peak Unity EdgeConnect
Dislosure: product version  
Source: URL  
Example:
```
{"usage":"append '?debug=requestinfo' to any querystring. Optional params: virtualPathCount",
"host":"_v5.02_Teloip Orchestrator API","hostType":"SelfHost (AppHostBase)",...}
```


## Talari SD-WAN
### Talari Appliance
Dislosure: product version  
Source: URL  
Example:
```
/css/talari.css?R7_3_QA_P1_D1_06152018
```


## SONUS SD-WAN
### SBC Edge
Dislosure: product version  
Source: HTML  
Example:
```
link rel="stylesheet" type="text/css" href="/style/6.1.2-471_rel_style_common.css">
<link rel="stylesheet" type="text/css" href="/style/6.1.2-471_rel_style.css">
```

### SBC Management Application
Dislosure: product version  
Source: HTML  
Example:
```
<div id="header_app_name">EMA 6.2 <span class="header_app_name_mode">[platform mode]</span></div>
```

## Arista Networks EOS
### Arista Switch
Dislosure: product version  
Source: SNMP  
Example:
```
Arista Networks EOS version 4.15.6M running on an Arista Networks DCS-7150S-24
```

## Glue Networks
### Gluware Control
Dislosure: product version  
Source: websocker
Example 1:
```
© 2018 Gluware, Inc. v3.3.98 (July 10, 2018 6:27am)
```

Example 2:
```
<content-bar-item>v3.3.98 (July 10, 2018 6:27am)</content-bar-item>
```
