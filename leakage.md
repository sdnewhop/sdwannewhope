# SD-WAN Version Leakage

## Overview
The most popular and known SD-WAN products leaking software versions are enumerated using search engines.

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
- [Cradlepoint](#cradlepoint)
- [Brain4Net](#brain4net)
- [Fortinet](#fortinet)

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
Dislosure: SSO
Source: JSON (`/versa/analytics/auth/sso/info`)
Example:
```
{"isSSOEnabled":false}

```
Dislosure: Full version  
Source: JSON (`/versa/analytics/version`)
Example:
```
{"package":"Versa Analytics","releaseDate":"Fri Nov 16 16:46:54 PST 2018","release":"16.1R2S6","dbVersion":"3.8.10","appId":"f23f3c","packageId":"f0fb84f","uiPackageId":"59819c3"}

```

Dislosure: Indirect analytics version  
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
Source: websocket  
Example 1:
```
© 2018 Gluware, Inc. v3.3.98 (July 10, 2018 6:27am)
```
Example 2:
```
<content-bar-item>v3.3.98 (July 10, 2018 6:27am)</content-bar-item>
```

## Cradlepoint
### Cradlepoint SD-WAN
Disclosure: product version  
Source: HTML  
Example (CR4250-PoE):  
```
<div id="displayfield-1031-inputEl" role="textbox" class="x-form-display-field x-form-display-field-default">6.6.4 (Thu Sep 27 20:58:36 UTC 2018)</div>
```
Example (AER2200-600M):
```
<div id="displayfield-1031-inputEl" role="textbox" class="x-form-display-field x-form-display-field-default">6.4.3 (Wed Dec 13 13:01:33 MST 2017)</div>
```

## Brain4Net
### Brain4Net Orchestrator
Disclosure: product version  
Source: JSON  
Example:  
```
{"api":"2.3.1","build":"2.4-FEATURE.ORC-2201","image":"orc-v2:4-FEATURE.ORC-2201"}
```
Example:
```
{
  "REACT_APP_NG_PORT" : 81,
  "REACT_APP_FRONTEND_WEB_PORT": 82,
  "REACT_APP_FRONTEND_TERM_PORT": 83,
  "REACT_APP_FRONTEND_STOMP_PORT": 84,
  "REACT_APP_VERSION": "2.4.932-SNAPSHOT"
}
```

## Fortinet
### Fortinet FortiGate Secure SD-WAN
Disclosure: build version, model  
Source: JavaScript (`fweb_all.js`)  
Example:  
```
CONFIG: {
    CONFIG_BUILD_NUMBER: 231,
    CONFIG_GUI_NO: "0cebad09e7db38e5316621c963cf944e",
    CONFIG_MAJOR_NUM: 6,
    CONFIG_MINOR_NUM: 0,
    CONFIG_MODEL: "FGT_81E_POE",
    CONFIG_MODEL_LEVEL_LOW: !0,
    CONFIG_PATCH_NUM: 4,
    CONFIG_SQL_LOG: !0
},
```
