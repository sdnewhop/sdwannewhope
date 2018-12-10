# SD-WAN Internet Census

## Overview
The most popular and known SD-WAN solutions are enumerated using search engines.

## Vendors
- [VMWare NSX SD-WAN](#vmware-nsx-sd-wan)
- [TELoIP VINO SD-WAN](#teloip-vino-sd-wan)
- [Fatpipe SYMPHONY SD-WAN](#fatpipe-symphony-sd-wan)
- [Cisco SD-WAN](#cisco-sd-wan)
- [Versa Networks](#versa-networks)
- [Riverbed SD-WAN](#riverbed-steelconnect)
- [Citrix NetScaler SD-WAN](#citrix-netscaler-sd-wan)
- [Silver Peak SD-WAN](#silver-peak)
- [CloudGenix SD-WAN](#cloudgenix-sd-wan)
- [Ecessa WANworX SD-WAN](#ecessa-wanworx-sd-wan)
- [Nuage Networks SD-WAN (VNS)](#nuage-networks-sd-wan-vns)
- [Juniper Networks Contrail SD-WAN](#juniper-networks-contrail-sd-wan)
- [Talari SD-WAN](#talari-sd-wan)
- [Aryaka SD-WAN](#aryaka-sd-wan)
- [InfoVista SD-WAN](#infovista-sd-wan)
- [Huawei SD-WAN](#huawei-sd-wan)
- [Sonus SD-WAN](#sonus-sd-wan)
- [Arista Networks EOS](#arista-networks-eos)
- [128 Technology](#128-technology)
- [Glue Networks](#glue-networks)
- [Barracuda Networks](#barracuda-networks)
- [Viprinet](#viprinet)
- [Cradlepoint](#cradlepoint)
- [Fortinet](#fortinet)
- [Brain4Net](#b4net)

## VMWare NSX SD-WAN
Confidence: Certain

### Google
* intitle:"Welcome to VeloCloud Page"
* "2013-2017 VeloCloud Networks"

### Shodan
* title:"VeloCloud"
* title:"VeloCloud Orchestrator"
* http.html_hash:1218757368
* http.favicon.hash:-2062596654 title:"301 Moved Permanently" 

### Censys
* 80.http.get.body:"VeloCloud Network Orchestrator"
* 80.http.get.body_sha256:ebaa382148c391357fa0976ccb8cf947a035e8be642190a4c9dff2c8a6ce1a0a

## TELoIP VINO SD-WAN
Confidence: Certain

### Google
* intitle:"Teloip Orchestrator API"
* "The following operations are supported. For a formal definition, please review the Service XSD."

### Shodan
* title:"Teloip Orchestrator API"

### Censys
* 80.http.get.body: "The following operations are supported. For a formal definition, please review the Service XSD." AND "Teloip Orchestrator API"

## Fatpipe SYMPHONY SD-WAN
Confidence: Certain

### Google
* inurl:/fpui/jsp/login.jsp
* intitle:"FatPipe WARP" "Log in"

### Shodan
* Linux Fatpipe
* title:"Fatpipe WARP" port:443

### Censys
* 80.http.get.title:"FatPipe WARP"
* 80.http.get.body_sha256: 81a46930a7041737c0c2b94299c14672e192ae4555fccd88cbc369755e84edc7

## Cisco SD-WAN
Confidence: Certain

### Google
* intitle:"Cisco vManage"
* intitle:"Viptela vManage"

### Shodan
* title:"Viptela vManage"
* title:"Cisco vManage"
* title:vManage
* http.favicon.hash:-904700687
* ssl:"O=Viptela Inc"

### Censys
* 80.http.get.title: "Viptela vManage"
* 80.http.get.title: "Cisco vManage"
* 80.http.get.body_sha256: 63575152efde5bec3ab2a28a502f7a15de7146e2b0fdce47ab0bb699676fb66f
* (443.https.tls.certificate.parsed.fingerprint_sha256: "ad4c8962d687837c54a3430e869aadfc359db7fd07d9b0630ec2f355aa7b896a" AND 443.https.tls.certificate.parsed.issuer.common_name: "vmanage") AND protocols.raw: "443/https"

## Versa Networks
Confidence: Certain

### Versa Analytics
#### Shodan
* versa-analytics port:161
* "van_analytics" port:9160
* ssl:"versa-analytics"

#### Censys
* 443.https.tls.certificate.parsed.issuer.common_name:"versa-analytics"

### Versa Flex VNF
#### Google
* intitle:"Flex VNF Web-UI"

#### Shodan
* title:"Flex VNF Web-UI"

#### Censys
* 80.http.get.body_sha256: 1d10f43efe5e0da430042178c7c8040d011bd5461279c5006ddabf867aae96cf
* 80.http.get.title: "Flex VNF Web-UI"

### Versa Director
#### Google
* inurl:"versa/app/login"
* intitle:"Versa Director Login"
* "2016 Versa Networks" "All Rights Reserved"
* "2017 Versa Networks" "All Rights Reserved"

#### Shodan
* "server: Versa Director"
* ssl:"VersaDirector"
* ssl:"versa-director"

#### Censys
* 80.http.get.body_sha256:867f6fead63c8809f208c735b87101c85629e404c762631f4ee47f95c07b6184
* 443.https.tls.certificate.parsed.subject_dn:"C=US, ST=California, O=versa-networks, OU=VersaDirector, CN=Director01"

## Riverbed 
Confidence: Certain

### Riverbed SteelConnect
### Google
* intitle:"SteelConnect Manager"

### Shodan
* title:"SteelConnect Manager"
* title:"Riverbed AWS Appliance"

### Censys
* 80.http.get.title:"Riverbed AWS Appliance"

### Riverbed SteelHead
### Google
* "Riverbed SteelHead" "Your browser may not be compatible."

### Shodan
* ssl:Riverbed Apache
* http.favicon.hash:-1338133217
* title:"amnesiac Sign in"

### Censys
* 80.http.get.body:"Riverbed SteelHead"
* "This SteelHead WAN optimization appliance is centrally managed as part of the AWS automation features within Riverbed SteelConnect."

## Citrix NetScaler SD-WAN
Confidence: Certain

### Citrix NetScaler SD-WAN VPX

### Google
* intitle:"Citrix NetScaler SD-WAN - Login"

### Shodan
* http.favicon.hash:-1272756243 title:"Citrix NetScaler SD-WAN - Login"
* title:"DC | Login" and ssl:"Citrix"

### Censys
* 443.https.tls.certificate.parsed.fingerprint_sha256:8199d53cf2832a133344559b09987b1d4830e643497f5f01d3178beb379ee7a5

### Citrix NetScaler SD-WAN Center
#### Google
* intitle:"SD-WAN Center | Login" -site:*.citrix.com

#### Shodan
* http.favicon.hash:-1272756243 title:"SD-WAN Center*Login"
* VWCSession

### Censys
* 80.http.get.title:"SD-WAN Center"
* 443.https.tls.certificate.parsed.names:mycitrixdemo.net AND `"<span>NetScaler</span>"`

## Silver Peak
Confidence: Certain

### Silver Peak Unity Orchestrator
### Google
* "Welcome to Unity Orchestrator"

### Shodan
* gmsSessionID
* SSL:"Silverpeak GMS"

### Censys
* 443.https.tls.certificate.parsed.subject.common_name: "Silverpeak GMS"

### Silver Peak Unity EdgeConnect
### Google
* "Silver Peak Appliance Management Console"

### Shodan
* vxoaSessionID
* ssl:"silver-peak"

### Censys
* 80.http.get.body: "By using this product, you agree to be bound by the terms of Silver Peak Systems Inc. " AND 443.https.tls.certificate.parsed.issuer.common_name: "silver-peak"

## CloudGenix SD-WAN
Confidence: Firm

### Shodan
* ssl:"O=CloudGenix Inc"

### Censys
* 443.https.tls.chain.parsed.issuer.organization:"CloudGenix Inc"

## Ecessa WANworX SD-WAN
Confidence: Tentative

### Google
* inurl:"/cgi-bin/pl_web.cgi/login1"

### Shodan
* http.html_hash:-1848258522 title:"Ecessa"

### Censys
* 80.http.get.body_sha256:7b9091bf0d0e65b6bcefa62a81dacc1d30fdf5344aa1d022865822a623aac987

## Nuage Networks SD-WAN (VNS)
Confidence: Certain

### Shodan
* title:"SD-WAN*Portal"
* http.favicon.hash:1069145589
* http.favicon.hash:1069145589 title:"SD-WAN*Portal"
* http.favicon.hash:1069145589 title:"Architect"
* http.favicon.hash:1069145589 title:"VNS portal"

### Censys
* 80.http.get.title:"SD-WAN Portal"
* 80.http.get.body_sha256:c0485f458c574e884168ba9fa07baf16ce86b761ac4dbf81dab9c0f87ed94ed2

## Juniper Networks Contrail SD-WAN
Confidence: Tentative

### Shodan
* title:"Log In - Juniper Networks Web Management"
* "Juniper Networks, Inc." junos srx

## Talari SD-WAN
Confidence: Certain

### Google
* inurl: "/cgi-bin/login.cgi"

### Shodan
* ssl:"emailAddress=support@talari.com"
* http.favicon.hash:269992656

### Censys
* 80.http.get.title:("AWS" AND "Login")
* 443.https.tls.certificate.parsed.issuer_dn:"C=US, ST=California, L=San Jose, O=Talari Networks, Inc., OU=Engineering, CN=Talari, emailAddress=support@talari.com"
* 443.https.tls.certificate.parsed.subject_key_info.fingerprint_sha256: f52b521dc30c3be76b9458f211eafd89fe63519678ff085f1c5c5cd7279a755d
* 80.http.get.body: "© 2017 Talari Networks"

## Aryaka SD-WAN
Confidence: Certain

### Aryaka Network Access Point
#### Google 
* intitle:"Aryaka, Welcome"

#### Shodan
* title:"Aryaka"
* "Aryaka Networks"
* http.favicon.hash:-1423557501
* title:"Aryaka, Welcome"

#### Censys
* 443.https.tls.certificate.parsed.subject.organization:"Aryaka Networks, Inc."

## InfoVista SD-WAN
Confidence: Certain

### InfoVista SALSA
#### Google
* inurl:"/salsa/salsa_portal/"

#### Shodan
* ssl:"SALSA Portal"
* "Server: Apache"+title:"SALSA"*"Login" port:443
* title:"SALSA Login"

#### Censys
* 80.http.get.title: ("SALSA" AND "Login")
* 443.https.tls.certificate.parsed.subject.organization: "Ipanema Technologies"
* 80.http.get.body_sha256:0cb459544a3772af457d2538c8de21c3e287e1920b4cc3f472fcd7a85d0acb14

## Huawei SD-WAN
Confidence: Certain

### Shodan
* title:"Agile Controller"

### Censys
* 80.http.get.title:"agile controller"
* 80.http.get.body_sha256:07f90f2912ebcf26b4b372a79e7ac91a2ff5f426e9aabc6b81b30298e18f47f6

## Sonus SD-WAN
Confidence: Certain

### Sonus SBC Management Application
#### Shodan
title:"SBC Management Application"

### Sonus SBC Edge
#### Shodan
* title:"Sonus SBC Edge Web Interface"

#### Censys
* 80.http.get.title: "Sonus SBC Edge Web Interface"

## Arista Networks
Confidence: Certain

### Arista Networks EOS
#### Shodan
* "Arista Networks EOS"

## 128 Technology
Confidence: Tentative

### 128 Technology Networking Platform
#### Shodan
* http.title:"128T Networking Platform"
* http.favicon.hash:-1556425248

#### Censys
* 80.http.get.title: "128T Networking Platform"

## Glue Networks
Confidence: Certain 

### Gluware Control
#### Shodan
* title:"Gluware Control"

#### Censys
* 80.http.get.title: "Gluware Control"

## Barracuda Networks
Confidence: Certain

### Barracuda CloudGen Firewall
#### Shodan
* ssl:"Barracuda CloudGen Firewall" port:"443"
* "Barracuda CloudGen Firewall"

#### Censys
* "Barracuda Cloudgen Firewall"

## Viprinet
Confidence: Certain

### Viprinet Virtual VPN Hub
#### Shodan
* Server: "Viprinet"
* Server: "ViprinetHubReplacement"
* title:"Viprinet - AdminDesk - Login"
* http.favicon.hash:-1352019987
* ssl: "Viprinet" port:"161"

#### Censys
* 80.http.get.headers.server:Viprinet
* 80.http.get.headers.server:ViprinetHubReplacement
* 80.http.get.title:"Viprinet - AdminDesk - Login"
* 80.http.get.body_sha256:1755d863bd2fbab47c2476af102bb42e8ae58f49927af6844b57258e5aa8fe8e

### Viprinet Traffic Tools
#### Shodan
* title:"Viprinet traffic tools"

#### Censys
* 80.http.get.title:"Viprinet traffic tools"

## Cradlepoint
Confidence: Certain

### Cradlepoint SD-WAN
#### Shodan
* title:"Login :: CR4250"
* title:"Login :: AER2200"

#### Censys
* 80.http.get.title: "Login :: AER2200-600M"
* 80.http.get.title: "Login :: CR4250-PoE"

## Fortinet
Confidence: Certain

### Fortinet FortiGate
#### Shodan
* ssl:"OU=FortiGate" ssl:"O=Fortinet" ssl:CN=FGT

#### Censys
* (443.https.tls.certificate.parsed.subject.organization: Fortinet) AND (443.https.tls.certificate.parsed.subject.common_name: FGT-*)

## Brain4Net
Confidence: Certain

### Brain4Net
#### Shodan
* title: B4N ORC

#### Censys
* 80.http.get.title: "B4N ORC"
