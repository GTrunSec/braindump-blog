+++
title = "Awesome Zeek"
date = 2020-11-22T00:00:00-08:00
lastmod = 2020-11-22T03:50:38-08:00
draft = false
creator = "Emacs 28.0.50 (Org mode 9.5 + ox-hugo)"
author = "GTrunSec"
+++

<style>
  .ox-hugo-toc ul {
    list-style: none;
  }
</style>
<div class="ox-hugo-toc toc">
<div></div>

<div class="heading">Table of Contents</div>

- <span class="section-num">1</span> [Zeek installation](#zeek-installation)
    - <span class="section-num">1.1</span> [Zeekurity Zen - Part I: How to Install Zeek on CentOS 8 - ericooi.com](#zeekurity-zen-part-i-how-to-install-zeek-on-centos-8-ericooi-dot-com)
        - <span class="section-num">1.1.1</span> [Zeekurity Zen Zeries - ericooi.com](#zeekurity-zen-zeries-ericooi-dot-com)
- <span class="section-num">2</span> [Zeek Documents](#zeek-documents)
    - <span class="section-num">2.1</span> [Zeek logging](#zeek-logging)
        - <span class="section-num">2.1.1</span> [Logging — Zeek User Manual v3.2.2](#logging-zeek-user-manual-v3-dot-2-dot-2)
        - <span class="section-num">2.1.2</span> [2019-04-cern-zeek-logging.pdf](#2019-04-cern-zeek-logging-dot-pdf)
    - <span class="section-num">2.2</span> [bro-in-90-minutes/mini-workshop.md at master · NSMAssociates/bro-in-90-minutes](#bro-in-90-minutes-mini-workshop-dot-md-at-master-nsmassociates-bro-in-90-minutes)
- <span class="section-num">3</span> [Zeek-cut](#zeek-cut)
    - <span class="section-num">3.1</span> [Using zeek-cut with logs](#using-zeek-cut-with-logs)
- <span class="section-num">4</span> [Zeek Performance](#zeek-performance)
    - <span class="section-num">4.1</span> [mozilla/zept: Zeek Extreme Performance Tuning](#mozilla-zept-zeek-extreme-performance-tuning)
- <span class="section-num">5</span> [Zeek Script](#zeek-script)
    - <span class="section-num">5.1</span> [Zeek Script Documents](#zeek-script-documents)
        - <span class="section-num">5.1.1</span> [Give me my stats!](#give-me-my-stats)
    - <span class="section-num">5.2</span> [Zeek Script tranning](#zeek-script-tranning)
        - <span class="section-num">5.2.1</span> [zeek/zeek-training: Zeek Training Materials/Products](#zeek-zeek-training-zeek-training-materials-products)
    - <span class="section-num">5.3</span> [ZeeK Script DNS<code>[3/3]</code>](#zeek-script-dns)
        - <span class="section-num">5.3.1</span> [<span class="org-todo done DONE">DONE</span> hhzzk/dns-tunnels](#hhzzk-dns-tunnels):DNS:
        - <span class="section-num">5.3.2</span> [<span class="org-todo done DONE">DONE</span> srozb/dns\_axfr: bro dns axfr package](#srozb-dns-axfr-bro-dns-axfr-package):DNS:
        - <span class="section-num">5.3.3</span> [<span class="org-todo done DONE">DONE</span> corelight/top-dns: Top DNS Measurement for Bro](#corelight-top-dns-top-dns-measurement-for-bro)
    - <span class="section-num">5.4</span> [Zeek Script Conn<code>[3/3]</code>](#zeek-script-conn)
        - <span class="section-num">5.4.1</span> [<span class="org-todo done DONE">DONE</span> corelight/bro-long-connections: Zeek package for tracking long connections to report them before they have completed.](#corelight-bro-long-connections-zeek-package-for-tracking-long-connections-to-report-them-before-they-have-completed-dot)
        - <span class="section-num">5.4.2</span> [<span class="org-todo done DONE">DONE</span> corelight/conn-burst: A Bro package to identify connections that are bursting (lots of data and transferring quickly).](#corelight-conn-burst-a-bro-package-to-identify-connections-that-are-bursting--lots-of-data-and-transferring-quickly--dot)
    - <span class="section-num">5.5</span> [Zeek Script SMB](#zeek-script-smb)
        - <span class="section-num">5.5.1</span> [Detecting Malicious SMB Activity Using Bro](#detecting-malicious-smb-activity-using-bro)
    - <span class="section-num">5.6</span> [Zeek Script SSL](#zeek-script-ssl)
        - <span class="section-num">5.6.1</span> [salesforce/ja3: JA3 is a standard for creating SSL client fingerprints in an easy to produce and shareable way.](#salesforce-ja3-ja3-is-a-standard-for-creating-ssl-client-fingerprints-in-an-easy-to-produce-and-shareable-way-dot)
        - <span class="section-num">5.6.2</span> [TLS client fingerprinting with Bro - Security Art Work](#tls-client-fingerprinting-with-bro-security-art-work)
        - <span class="section-num">5.6.3</span> [Onion-Zeek-RITA: Improving Network Visibility and Detecting C2 Activity](#onion-zeek-rita-improving-network-visibility-and-detecting-c2-activity)
        - <span class="section-num">5.6.4</span> [Detecting Tor traffic with Bro network traffic analyzer - Stephen Reese](#detecting-tor-traffic-with-bro-network-traffic-analyzer-stephen-reese)
    - <span class="section-num">5.7</span> [Zeek Script logging](#zeek-script-logging)
        - <span class="section-num">5.7.1</span> [Zeek logs to database](#zeek-logs-to-database)
        - <span class="section-num">5.7.2</span> [corelight/zeek-community-id: Zeek support for "community ID" flow hashing.](#corelight-zeek-community-id-zeek-support-for-community-id-flow-hashing-dot)
    - <span class="section-num">5.8</span> [Zeek logs to json](#zeek-logs-to-json)
        - <span class="section-num">5.8.1</span> [add-json/add-json.zeek at master · J-Gras/add-json](#add-json-add-json-dot-zeek-at-master-j-gras-add-json)
        - <span class="section-num">5.8.2</span> [corelight/json-streaming-logs: Bro script package to create JSON formatted logs to stream into data analysis systems.](#corelight-json-streaming-logs-bro-script-package-to-create-json-formatted-logs-to-stream-into-data-analysis-systems-dot)
    - <span class="section-num">5.9</span> [Zeel Vlan](#zeel-vlan)
        - <span class="section-num">5.9.1</span> [https://github.com/corelight/log-add-vlan-everywhere](#https-github-dot-com-corelight-log-add-vlan-everywhere)
    - <span class="section-num">5.10</span> [Zeek CVE Detection](#zeek-cve-detection)
        - <span class="section-num">5.10.1</span> [GitHub - corelight/CVE-2020-16898: A network detection package for CVE-2020-16898 (Windows TCP/IP Remote Code Execution Vulnerability)](#github-corelight-cve-2020-16898-a-network-detection-package-for-cve-2020-16898--windows-tcp-ip-remote-code-execution-vulnerability):windows:
        - <span class="section-num">5.10.2</span> [GitHub - 0xxon/cve-2020-0601: Zeek package to detect CVE-2020-0601](#github-0xxon-cve-2020-0601-zeek-package-to-detect-cve-2020-0601)
        - <span class="section-num">5.10.3</span> [0xxon/cve-2020-13777: Zeek script to detect servers vulnerable to CVE-2020-13777](#0xxon-cve-2020-13777-zeek-script-to-detect-servers-vulnerable-to-cve-2020-13777)
        - <span class="section-num">5.10.4</span> [0xxon/zeek-plugin-roca: Bro plugin to check if certificates are affected by CVE-2017-15361](#0xxon-zeek-plugin-roca-bro-plugin-to-check-if-certificates-are-affected-by-cve-2017-15361)
        - <span class="section-num">5.10.5</span> [initconf/CVE-2017-5638\_struts: detection for Apache Struts recon and compromise](#initconf-cve-2017-5638-struts-detection-for-apache-struts-recon-and-compromise)
    - <span class="section-num">5.11</span> [Zeek detect software](#zeek-detect-software)
        - <span class="section-num">5.11.1</span> [fatemabw/bro-inventory-scripts](#fatemabw-bro-inventory-scripts)
    - <span class="section-num">5.12</span> [Zeek services detection](#zeek-services-detection)
        - <span class="section-num">5.12.1</span> [hosom/odd-services: Detect weird services on a network.](#hosom-odd-services-detect-weird-services-on-a-network-dot)
    - <span class="section-num">5.13</span> [Zeek Scanner](#zeek-scanner)
        - <span class="section-num">5.13.1</span> [JonZeolla/scan-sampling: Moyified version of scan.bro to add destination IP sampling](#jonzeolla-scan-sampling-moyified-version-of-scan-dot-bro-to-add-destination-ip-sampling)
        - <span class="section-num">5.13.2</span> [ncsa/bro-simple-scan](#ncsa-bro-simple-scan)
        - <span class="section-num">5.13.3</span> [ncsa/bro-is-darknet](#ncsa-bro-is-darknet)
        - <span class="section-num">5.13.4</span> [initconf/scan-NG: scan-detection policies for bro](#initconf-scan-ng-scan-detection-policies-for-bro)
    - <span class="section-num">5.14</span> [Zeek files detection](#zeek-files-detection)
        - <span class="section-num">5.14.1</span> [hosom/file-extraction: Extract files from network traffic with Zeek.](#hosom-file-extraction-extract-files-from-network-traffic-with-zeek-dot)
        - <span class="section-num">5.14.2</span> [theflakes/bro-large\_uploads](#theflakes-bro-large-uploads)
        - <span class="section-num">5.14.3</span> [corelight/bro-xor-exe-plugin: Bro plugin to detect and decrypt XOR-encrypted EXEs](#corelight-bro-xor-exe-plugin-bro-plugin-to-detect-and-decrypt-xor-encrypted-exes)
    - <span class="section-num">5.15</span> [Zeek RDP detection](#zeek-rdp-detection)
        - <span class="section-num">5.15.1</span> [theparanoids/rdfp: Remote Desktop Client Fingerprint script for Zeek. Based off of https://github.com/0x4D31/fatt](#theparanoids-rdfp-remote-desktop-client-fingerprint-script-for-zeek-dot-based-off-of-https-github-dot-com-0x4d31-fatt)
        - <span class="section-num">5.15.2</span> [initconf/RDP-bruteforce: RDP bruteforce detection](#initconf-rdp-bruteforce-rdp-bruteforce-detection)
    - <span class="section-num">5.16</span> [Zeek misc detection](#zeek-misc-detection)
        - <span class="section-num">5.16.1</span> [jsiwek/zeek-cryptomining: Detect cryptocurrency mining traffic with Zeek.](#jsiwek-zeek-cryptomining-detect-cryptocurrency-mining-traffic-with-zeek-dot)
        - <span class="section-num">5.16.2</span> [bro-inventory-scripts/scripts at master · fatemabw/bro-inventory-scripts](#bro-inventory-scripts-scripts-at-master-fatemabw-bro-inventory-scripts)
        - <span class="section-num">5.16.3</span> [vnc-scanner/scripts at master · initconf/vnc-scanner](#vnc-scanner-scripts-at-master-initconf-vnc-scanner)
        - <span class="section-num">5.16.4</span> [corelight/bro-drwatson: Dr. Watson catcher script for Bro.](#corelight-bro-drwatson-dr-dot-watson-catcher-script-for-bro-dot)
        - <span class="section-num">5.16.5</span> [rpot/Mac-version-detection.bro at master · tatsu-i/rpot](#rpot-mac-version-detection-dot-bro-at-master-tatsu-i-rpot)
        - <span class="section-num">5.16.6</span> [<span class="org-todo todo TODO">TODO</span> sheharbano/BotFlex: BotFlex is an open source tool or bot detection and analysis](#sheharbano-botflex-botflex-is-an-open-source-tool-or-bot-detection-and-analysis):learn:
        - <span class="section-num">5.16.7</span> [<span class="org-todo todo TODO">TODO</span> bro\_capstone/scripts at master · empick94/bro\_capstone](#bro-capstone-scripts-at-master-empick94-bro-capstone):learn:
    - <span class="section-num">5.17</span> [Zeek attack detection](#zeek-attack-detection)
        - <span class="section-num">5.17.1</span> [initconf/sip-attacks: zeek Package to detect attacks in SIP protocol](#initconf-sip-attacks-zeek-package-to-detect-attacks-in-sip-protocol)
    - <span class="section-num">5.18</span> [Zeek virus detection](#zeek-virus-detection)
        - <span class="section-num">5.18.1</span> [initconf/detect-kaspersky: Bro package to detect kaspersky anti-virus in your network](#initconf-detect-kaspersky-bro-package-to-detect-kaspersky-anti-virus-in-your-network)
        - <span class="section-num">5.18.2</span> [dopheide/venom](#dopheide-venom)
        - <span class="section-num">5.18.3</span> [secured-psa-nsm/PSA/modules at master · SECURED-FP7/secured-psa-nsm](#secured-psa-nsm-psa-modules-at-master-secured-fp7-secured-psa-nsm)
    - <span class="section-num">5.19</span> [Zeek SMTP](#zeek-smtp)
        - <span class="section-num">5.19.1</span> [initconf/phish-analysis: Suite of smtp related policies includes extracting and logging URLs from emails and various smtp anomaly detection heuristics to help flag phishing emails](#initconf-phish-analysis-suite-of-smtp-related-policies-includes-extracting-and-logging-urls-from-emails-and-various-smtp-anomaly-detection-heuristics-to-help-flag-phishing-emails)
        - <span class="section-num">5.19.2</span> [initconf/smtp-url-analysis: Extracting and analyzing URLs from Emails for phishing events](#initconf-smtp-url-analysis-extracting-and-analyzing-urls-from-emails-for-phishing-events)
- <span class="section-num">6</span> [Zeek Plugin or analyzer](#zeek-plugin-or-analyzer)
    - <span class="section-num">6.1</span> [J-Gras/zeek-af\_packet-plugin: Plugin providing native AF\_Packet support for Zeek (formerly known as Bro).](#j-gras-zeek-af-packet-plugin-plugin-providing-native-af-packet-support-for-zeek--formerly-known-as-bro--dot)
    - <span class="section-num">6.2</span> [<span class="org-todo done DONE">DONE</span> GitHub - reservoirlabs/zeek-zip-analyzer: ZIP analyzer for Zeek](#github-reservoirlabs-zeek-zip-analyzer-zip-analyzer-for-zeek):analyzer:
    - <span class="section-num">6.3</span> [bro-netmap/zkg.meta at master · zeek/bro-netmap · GitHub](#bro-netmap-zkg-dot-meta-at-master-zeek-bro-netmap-github):packet:
    - <span class="section-num">6.4</span> [J-Gras/bro-lognorm: Bro plugin providing liblognorm integration.](#j-gras-bro-lognorm-bro-plugin-providing-liblognorm-integration-dot)
    - <span class="section-num">6.5</span> [<span class="org-todo done __CANCELED">✘ CANCELED</span> jswaro/tcprs: TCP Retransmission and State Analyzer plugin for the Bro-IDS framework](#jswaro-tcprs-tcp-retransmission-and-state-analyzer-plugin-for-the-bro-ids-framework)
    - <span class="section-num">6.6</span> [dopheide-esnet/bro-quic: Analyzer that attempts to identify the QUIC protocol.](#dopheide-esnet-bro-quic-analyzer-that-attempts-to-identify-the-quic-protocol-dot)
- <span class="section-num">7</span> [Zeek Threat Intelligence(Intel)](#zeek-threat-intelligence--intel)
    - <span class="section-num">7.1</span> [blacklist/scripts at master · initconf/blacklist](#blacklist-scripts-at-master-initconf-blacklist)
    - <span class="section-num">7.2</span> [kinomakino/Threat-Intelligence-Data: Snort\_rules detection bad actors.](#kinomakino-threat-intelligence-data-snort-rules-detection-bad-actors-dot)
- <span class="section-num">8</span> [Zeek Cluster](#zeek-cluster)
    - <span class="section-num">8.1</span> [J-Gras/add-node-names: Adds cluster node name to logs.](#j-gras-add-node-names-adds-cluster-node-name-to-logs-dot)
- <span class="section-num">9</span> [Zeek Agent](#zeek-agent)
    - <span class="section-num">9.1</span> [zeek/zeek-agent: An endpoint monitoring agent that provides host activity to Zeek](#zeek-zeek-agent-an-endpoint-monitoring-agent-that-provides-host-activity-to-zeek)
    - <span class="section-num">9.2</span> [zeek/bro-netmap: Native Netmap Packet IOSource for Bro/Zeek](#zeek-bro-netmap-native-netmap-packet-iosource-for-bro-zeek)
    - <span class="section-num">9.3</span> [<span class="org-todo done DONE">DONE</span> apache/metron-bro-plugin-kafka: Apache Metron](#apache-metron-bro-plugin-kafka-apache-metron):agent:
    - <span class="section-num">9.4</span> [<span class="org-todo done DONE">DONE</span> zeek-postgresql/scripts at master · 0xxon/zeek-postgresql](#zeek-postgresql-scripts-at-master-0xxon-zeek-postgresql):agent:
    - <span class="section-num">9.5</span> [ncsa/bro-zeromq-writer: Bro plugin that provides a ZeroMQ log writer.](#ncsa-bro-zeromq-writer-bro-plugin-that-provides-a-zeromq-log-writer-dot)
- <span class="section-num">10</span> [Zeek Con](#zeek-con)
    - <span class="section-num">10.1</span> [Virtual ZeekWeek](#virtual-zeekweek)
        - <span class="section-num">10.1.1</span> [Virtual ZeekWeek 2020: Day 3 - YouTube](#virtual-zeekweek-2020-day-3-youtube)
- <span class="section-num">11</span> [Zeek ThirdParty Support](#zeek-thirdparty-support)
    - <span class="section-num">11.1</span> [joesecurity/Joe-Sandbox-Bro: JoeSandbox-Bro is a simple bro script which extracts files from your internet connection and analyzes them automatically on Joe Sandbox](#joesecurity-joe-sandbox-bro-joesandbox-bro-is-a-simple-bro-script-which-extracts-files-from-your-internet-connection-and-analyzes-them-automatically-on-joe-sandbox)
- <span class="section-num">12</span> [Zeek troubleshoot](#zeek-troubleshoot)
    - <span class="section-num">12.1</span> [ncsa/bro-doctor](#ncsa-bro-doctor)
- <span class="section-num">13</span> [Zeek deployment](#zeek-deployment)
    - <span class="section-num">13.1</span> [ncsa/bro-interface-setup](#ncsa-bro-interface-setup)
- <span class="section-num">14</span> [Zeek Notice or alert](#zeek-notice-or-alert)
    - <span class="section-num">14.1</span> [pgaulon/zeek-notice-slack: Script extending Zeek Notice framework, adding Slack notifications](#pgaulon-zeek-notice-slack-script-extending-zeek-notice-framework-adding-slack-notifications)
- <span class="section-num">15</span> [Zeek Lang expression](#zeek-lang-expression)
    - <span class="section-num">15.1</span> [Zeek: Zeke on Zeek: Working With Open-Source Zeek: Adding a Key-value For-Loop](#zeek-zeke-on-zeek-working-with-open-source-zeek-adding-a-key-value-for-loop)
- <span class="section-num">16</span> [Zeek to kafka](#zeek-to-kafka)
    - <span class="section-num">16.1</span> [nickwallen’s gists](#nickwallen-s-gists)

</div>
<!--endtoc-->

tags
: [Network monitoring]({{< relref "nsm" >}})


[Slack | general | Zeek | 1 new item](https://app.slack.com/client/TSXGCHZE1/CSZBXF6TH)


## <span class="section-num">1</span> Zeek installation {#zeek-installation}


### <span class="section-num">1.1</span> [Zeekurity Zen - Part I: How to Install Zeek on CentOS 8 - ericooi.com](https://www.ericooi.com/zeekurity-zen-part-i-how-to-install-zeek-on-centos-8/#comment-1670) {#zeekurity-zen-part-i-how-to-install-zeek-on-centos-8-ericooi-dot-com}


#### <span class="section-num">1.1.1</span> [Zeekurity Zen Zeries - ericooi.com](https://www.ericooi.com/zeekurity-zen-zeries/) {#zeekurity-zen-zeries-ericooi-dot-com}


## <span class="section-num">2</span> Zeek Documents {#zeek-documents}


### <span class="section-num">2.1</span> Zeek logging {#zeek-logging}

-   [Slide 1](http://gauss.ececs.uc.edu/Courses/c6055/pdf/bro%5Flog%5Fvars.pdf)


#### <span class="section-num">2.1.1</span> [Logging — Zeek User Manual v3.2.2](https://docs.zeek.org/en/current/examples/logs/) {#logging-zeek-user-manual-v3-dot-2-dot-2}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-10-14 Wed 23:50] </span></span> <- [Using zeek-cut with logs](#using-zeek-cut-with-logs)


#### <span class="section-num">2.1.2</span> [2019-04-cern-zeek-logging.pdf](https://indico.cern.ch/event/762505/contributions/3375201/attachments/1830709/2998002/2019-04-cern-zeek-logging.pdf) {#2019-04-cern-zeek-logging-dot-pdf}


### <span class="section-num">2.2</span> [bro-in-90-minutes/mini-workshop.md at master · NSMAssociates/bro-in-90-minutes](https://github.com/NSMAssociates/bro-in-90-minutes/blob/master/mini-workshop.md) {#bro-in-90-minutes-mini-workshop-dot-md-at-master-nsmassociates-bro-in-90-minutes}


## <span class="section-num">3</span> Zeek-cut {#zeek-cut}


### <span class="section-num">3.1</span> Using zeek-cut with logs {#using-zeek-cut-with-logs}

-   [Logging — Zeek User Manual v3.2.2](#logging-zeek-user-manual-v3-dot-2-dot-2)


## <span class="section-num">4</span> Zeek Performance {#zeek-performance}


### <span class="section-num">4.1</span> [mozilla/zept: Zeek Extreme Performance Tuning](https://github.com/mozilla/zept) {#mozilla-zept-zeek-extreme-performance-tuning}


## <span class="section-num">5</span> Zeek Script {#zeek-script}

-   [packages/aggregate.meta at master · zeek/packages](https://github.com/zeek/packages/blob/master/aggregate.meta)
    -   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:12] </span></span> -> [corelight/bro-shellshock: ShellShock attack and exploit detector for Bro.](security.md)


### <span class="section-num">5.1</span> Zeek Script Documents {#zeek-script-documents}


#### <span class="section-num">5.1.1</span> [Give me my stats!](https://corelight.blog/2020/09/21/give-me-my-stats/) {#give-me-my-stats}


### <span class="section-num">5.2</span> Zeek Script tranning {#zeek-script-tranning}


#### <span class="section-num">5.2.1</span> [zeek/zeek-training: Zeek Training Materials/Products](https://github.com/zeek/zeek-training) {#zeek-zeek-training-zeek-training-materials-products}


### <span class="section-num">5.3</span> ZeeK Script DNS<code>[3/3]</code> {#zeek-script-dns}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-20 Fri 21:22] </span></span> <- [Network Security Project or Idea DNS](network.md)


#### <span class="org-todo done DONE">DONE</span> <span class="section-num">5.3.1</span> [hhzzk/dns-tunnels](https://github.com/hhzzk/dns-tunnels) {#hhzzk-dns-tunnels}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-20 Fri 21:31] </span></span> -> [detecting-dns-tunneling](network.md)


#### <span class="org-todo done DONE">DONE</span> <span class="section-num">5.3.2</span> [srozb/dns\_axfr: bro dns axfr package](https://github.com/srozb/dns%5Faxfr) {#srozb-dns-axfr-bro-dns-axfr-package}

-   [DNS zone transfer - Wikipedia](https://en.wikipedia.org/wiki/DNS%5Fzone%5Ftransfer)
-   [https://cr.yp.to/djbdns/axfr-notes.html](https://cr.yp.to/djbdns/axfr-notes.html)


#### <span class="org-todo done DONE">DONE</span> <span class="section-num">5.3.3</span> [corelight/top-dns: Top DNS Measurement for Bro](https://github.com/corelight/top-dns) {#corelight-top-dns-top-dns-measurement-for-bro}


### <span class="section-num">5.4</span> Zeek Script Conn<code>[3/3]</code> {#zeek-script-conn}


#### <span class="org-todo done DONE">DONE</span> <span class="section-num">5.4.1</span> [corelight/bro-long-connections: Zeek package for tracking long connections to report them before they have completed.](https://github.com/corelight/bro-long-connections) {#corelight-bro-long-connections-zeek-package-for-tracking-long-connections-to-report-them-before-they-have-completed-dot}


#### <span class="org-todo done DONE">DONE</span> <span class="section-num">5.4.2</span> [corelight/conn-burst: A Bro package to identify connections that are bursting (lots of data and transferring quickly).](https://github.com/corelight/conn-burst) {#corelight-conn-burst-a-bro-package-to-identify-connections-that-are-bursting--lots-of-data-and-transferring-quickly--dot}


### <span class="section-num">5.5</span> Zeek Script SMB {#zeek-script-smb}


#### <span class="section-num">5.5.1</span> [Detecting Malicious SMB Activity Using Bro](https://www.giac.org/paper/gcia/10091/detecting-malicious-smb-activity-bro/140938) {#detecting-malicious-smb-activity-using-bro}


### <span class="section-num">5.6</span> Zeek Script SSL {#zeek-script-ssl}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 01:58] </span></span> -> [Network Security SSL](network.md)
-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:01] </span></span> -> [Onion-Zeek-RITA: Improving Network Visibility and Detecting C2 Activity](security.md)


#### <span class="section-num">5.6.1</span> [salesforce/ja3: JA3 is a standard for creating SSL client fingerprints in an easy to produce and shareable way.](https://github.com/salesforce/ja3) {#salesforce-ja3-ja3-is-a-standard-for-creating-ssl-client-fingerprints-in-an-easy-to-produce-and-shareable-way-dot}


#### <span class="section-num">5.6.2</span> [TLS client fingerprinting with Bro - Security Art Work](https://www.securityartwork.es/2017/02/02/tls-client-fingerprinting-with-bro/) {#tls-client-fingerprinting-with-bro-security-art-work}


#### <span class="section-num">5.6.3</span> [Onion-Zeek-RITA: Improving Network Visibility and Detecting C2 Activity](https://www.sans.org/reading-room/whitepapers/detection/onion-zeek-rita-improving-network-visibility-detecting-c2-activity-38755) {#onion-zeek-rita-improving-network-visibility-and-detecting-c2-activity}


#### <span class="section-num">5.6.4</span> [Detecting Tor traffic with Bro network traffic analyzer - Stephen Reese](https://www.rsreese.com/detecting-tor-traffic-with-bro-network-traffic-analyzer/) {#detecting-tor-traffic-with-bro-network-traffic-analyzer-stephen-reese}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:04] </span></span> -> [Network Tor](network.md)


### <span class="section-num">5.7</span> Zeek Script logging {#zeek-script-logging}

-   [filter] <https://github.com/hosom/log-filters>


#### <span class="section-num">5.7.1</span> Zeek logs to database {#zeek-logs-to-database}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:10] </span></span> <- [zeek-postgresql/scripts at master · 0xxon/zeek-postgresql](#zeek-postgresql-scripts-at-master-0xxon-zeek-postgresql)
    -   [ ] database
    -   [Creating user, database and adding access on PostgreSQL](https://medium.com/coding-blocks/creating-user-database-and-adding-access-on-postgresql-8bfcd2f4a91e)

        ```sh
        sudo -u postgres psql
        sudo -u postgres createuser <username>
        sudo -u postgres createdb <dbname>
        createdb -h localhost -p 5432 -U dbuser testdb
        psql -h localhost -p 5432 -U dbuser -d testdb

        ```


#### <span class="section-num">5.7.2</span> [corelight/zeek-community-id: Zeek support for "community ID" flow hashing.](https://github.com/corelight/zeek-community-id) {#corelight-zeek-community-id-zeek-support-for-community-id-flow-hashing-dot}


### <span class="section-num">5.8</span> Zeek logs to json {#zeek-logs-to-json}


#### <span class="section-num">5.8.1</span> [add-json/add-json.zeek at master · J-Gras/add-json](https://github.com/J-Gras/add-json/blob/master/scripts/add-json.zeek) {#add-json-add-json-dot-zeek-at-master-j-gras-add-json}

-   [Working with JSON in bash using jq - Cameron Nokes](https://cameronnokes.com/blog/working-with-json-in-bash-using-jq/)


#### <span class="section-num">5.8.2</span> [corelight/json-streaming-logs: Bro script package to create JSON formatted logs to stream into data analysis systems.](https://github.com/corelight/json-streaming-logs) {#corelight-json-streaming-logs-bro-script-package-to-create-json-formatted-logs-to-stream-into-data-analysis-systems-dot}


### <span class="section-num">5.9</span> Zeel Vlan {#zeel-vlan}


#### <span class="section-num">5.9.1</span> <https://github.com/corelight/log-add-vlan-everywhere> {#https-github-dot-com-corelight-log-add-vlan-everywhere}


### <span class="section-num">5.10</span> Zeek CVE Detection {#zeek-cve-detection}


#### <span class="section-num">5.10.1</span> [GitHub - corelight/CVE-2020-16898: A network detection package for CVE-2020-16898 (Windows TCP/IP Remote Code Execution Vulnerability)](https://github.com/corelight/CVE-2020-16898) {#github-corelight-cve-2020-16898-a-network-detection-package-for-cve-2020-16898--windows-tcp-ip-remote-code-execution-vulnerability}


#### <span class="section-num">5.10.2</span> [GitHub - 0xxon/cve-2020-0601: Zeek package to detect CVE-2020-0601](https://github.com/0xxon/cve-2020-0601) {#github-0xxon-cve-2020-0601-zeek-package-to-detect-cve-2020-0601}


#### <span class="section-num">5.10.3</span> [0xxon/cve-2020-13777: Zeek script to detect servers vulnerable to CVE-2020-13777](https://github.com/0xxon/cve-2020-13777) {#0xxon-cve-2020-13777-zeek-script-to-detect-servers-vulnerable-to-cve-2020-13777}


#### <span class="section-num">5.10.4</span> [0xxon/zeek-plugin-roca: Bro plugin to check if certificates are affected by CVE-2017-15361](https://github.com/0xxon/zeek-plugin-roca) {#0xxon-zeek-plugin-roca-bro-plugin-to-check-if-certificates-are-affected-by-cve-2017-15361}


#### <span class="section-num">5.10.5</span> [initconf/CVE-2017-5638\_struts: detection for Apache Struts recon and compromise](https://github.com/initconf/CVE-2017-5638%5Fstruts) {#initconf-cve-2017-5638-struts-detection-for-apache-struts-recon-and-compromise}


### <span class="section-num">5.11</span> Zeek detect software {#zeek-detect-software}


#### <span class="section-num">5.11.1</span> [fatemabw/bro-inventory-scripts](https://github.com/fatemabw/bro-inventory-scripts) {#fatemabw-bro-inventory-scripts}

This package contains the scripts that can be used with Bro to detect different software running on clients, specially fingerprinting the clients in your network. By default the AV detection script is not loaded.


### <span class="section-num">5.12</span> Zeek services detection {#zeek-services-detection}


#### <span class="section-num">5.12.1</span> [hosom/odd-services: Detect weird services on a network.](https://github.com/hosom/odd-services) {#hosom-odd-services-detect-weird-services-on-a-network-dot}


### <span class="section-num">5.13</span> Zeek Scanner {#zeek-scanner}


#### <span class="section-num">5.13.1</span> [JonZeolla/scan-sampling: Moyified version of scan.bro to add destination IP sampling](https://github.com/JonZeolla/scan-sampling) {#jonzeolla-scan-sampling-moyified-version-of-scan-dot-bro-to-add-destination-ip-sampling}


#### <span class="section-num">5.13.2</span> [ncsa/bro-simple-scan](https://github.com/ncsa/bro-simple-scan) {#ncsa-bro-simple-scan}


#### <span class="section-num">5.13.3</span> [ncsa/bro-is-darknet](https://github.com/ncsa/bro-is-darknet) {#ncsa-bro-is-darknet}

This plugin adds a Site::is\_darknet function. This is useful for scripts that track scan attempts or other probes. It can handle purely dark address space as well as honeynet space.


#### <span class="section-num">5.13.4</span> [initconf/scan-NG: scan-detection policies for bro](https://github.com/initconf/scan-NG) {#initconf-scan-ng-scan-detection-policies-for-bro}


### <span class="section-num">5.14</span> Zeek files detection {#zeek-files-detection}


#### <span class="section-num">5.14.1</span> [hosom/file-extraction: Extract files from network traffic with Zeek.](https://github.com/hosom/file-extraction) {#hosom-file-extraction-extract-files-from-network-traffic-with-zeek-dot}


#### <span class="section-num">5.14.2</span> [theflakes/bro-large\_uploads](https://github.com/theflakes/bro-large%5Fuploads) {#theflakes-bro-large-uploads}


#### <span class="section-num">5.14.3</span> [corelight/bro-xor-exe-plugin: Bro plugin to detect and decrypt XOR-encrypted EXEs](https://github.com/corelight/bro-xor-exe-plugin) {#corelight-bro-xor-exe-plugin-bro-plugin-to-detect-and-decrypt-xor-encrypted-exes}

Bro plugin to detect and decrypt XOR-obfuscated Windows EXEs.


### <span class="section-num">5.15</span> Zeek RDP detection {#zeek-rdp-detection}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:37] </span></span> -> [Remote Desktop Services](network.md)


#### <span class="section-num">5.15.1</span> [theparanoids/rdfp: Remote Desktop Client Fingerprint script for Zeek. Based off of https://github.com/0x4D31/fatt](https://github.com/theparanoids/rdfp) {#theparanoids-rdfp-remote-desktop-client-fingerprint-script-for-zeek-dot-based-off-of-https-github-dot-com-0x4d31-fatt}


#### <span class="section-num">5.15.2</span> [initconf/RDP-bruteforce: RDP bruteforce detection](https://github.com/initconf/RDP-bruteforce) {#initconf-rdp-bruteforce-rdp-bruteforce-detection}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 03:50] </span></span> -> [Brute force attacks increase due to more open RDP ports - Malwarebytes Labs | Malwarebytes Labs](network.md)


### <span class="section-num">5.16</span> Zeek misc detection {#zeek-misc-detection}


#### <span class="section-num">5.16.1</span> [jsiwek/zeek-cryptomining: Detect cryptocurrency mining traffic with Zeek.](https://github.com/jsiwek/zeek-cryptomining) {#jsiwek-zeek-cryptomining-detect-cryptocurrency-mining-traffic-with-zeek-dot}

This script/package for Zeek can detect Bitcoin, Litecoin, PPCoin, or other cryptocurrency mining traffic that uses getwork, getblocktemplate, or Stratum mining protocols over TCP or HTTP. Note that the module cannot currently detect the Bitcoin P2P protocol, which is different from the mining protocols.


#### <span class="section-num">5.16.2</span> [bro-inventory-scripts/scripts at master · fatemabw/bro-inventory-scripts](https://github.com/fatemabw/bro-inventory-scripts/tree/master/scripts) {#bro-inventory-scripts-scripts-at-master-fatemabw-bro-inventory-scripts}


#### <span class="section-num">5.16.3</span> [vnc-scanner/scripts at master · initconf/vnc-scanner](https://github.com/initconf/vnc-scanner/tree/master/scripts) {#vnc-scanner-scripts-at-master-initconf-vnc-scanner}

Simple policy to detect VNC (RFB) scanners based on src->dst connection counts


#### <span class="section-num">5.16.4</span> [corelight/bro-drwatson: Dr. Watson catcher script for Bro.](https://github.com/corelight/bro-drwatson) {#corelight-bro-drwatson-dr-dot-watson-catcher-script-for-bro-dot}

Microsoft sends diagnostic information back to themselves through a mechism named Dr. Watson. The initial "StageOne" is unencrypted and sent over HTTP so it's visible to Bro. This script takes the StageOne messages and parses all available information out of them to create a series of logs.


#### <span class="section-num">5.16.5</span> [rpot/Mac-version-detection.bro at master · tatsu-i/rpot](https://github.com/tatsu-i/rpot/blob/master/bro/bro%5Fconfig/scripts/misc/Mac-version-detection.bro) {#rpot-mac-version-detection-dot-bro-at-master-tatsu-i-rpot}


#### <span class="org-todo todo TODO">TODO</span> <span class="section-num">5.16.6</span> [sheharbano/BotFlex: BotFlex is an open source tool or bot detection and analysis](https://github.com/sheharbano/BotFlex) {#sheharbano-botflex-botflex-is-an-open-source-tool-or-bot-detection-and-analysis}


#### <span class="org-todo todo TODO">TODO</span> <span class="section-num">5.16.7</span> [bro\_capstone/scripts at master · empick94/bro\_capstone](https://github.com/empick94/bro%5Fcapstone/tree/master/scripts) {#bro-capstone-scripts-at-master-empick94-bro-capstone}


### <span class="section-num">5.17</span> Zeek attack detection {#zeek-attack-detection}


#### <span class="section-num">5.17.1</span> [initconf/sip-attacks: zeek Package to detect attacks in SIP protocol](https://github.com/initconf/sip-attacks) {#initconf-sip-attacks-zeek-package-to-detect-attacks-in-sip-protocol}


### <span class="section-num">5.18</span> Zeek virus detection {#zeek-virus-detection}


#### <span class="section-num">5.18.1</span> [initconf/detect-kaspersky: Bro package to detect kaspersky anti-virus in your network](https://github.com/initconf/detect-kaspersky/) {#initconf-detect-kaspersky-bro-package-to-detect-kaspersky-anti-virus-in-your-network}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:33] </span></span> -> [Kaspersky Anti-Virus](security.md)


#### <span class="section-num">5.18.2</span> [dopheide/venom](https://github.com/dopheide/venom) {#dopheide-venom}

This package attempts to detect scanners searching for the VENOM vulnerability. Cluster communication is fully supported.


#### <span class="section-num">5.18.3</span> [secured-psa-nsm/PSA/modules at master · SECURED-FP7/secured-psa-nsm](https://github.com/SECURED-FP7/secured-psa-nsm/tree/master/PSA/modules) {#secured-psa-nsm-psa-modules-at-master-secured-fp7-secured-psa-nsm}


### <span class="section-num">5.19</span> Zeek SMTP {#zeek-smtp}


#### <span class="section-num">5.19.1</span> [initconf/phish-analysis: Suite of smtp related policies includes extracting and logging URLs from emails and various smtp anomaly detection heuristics to help flag phishing emails](https://github.com/initconf/phish-analysis) {#initconf-phish-analysis-suite-of-smtp-related-policies-includes-extracting-and-logging-urls-from-emails-and-various-smtp-anomaly-detection-heuristics-to-help-flag-phishing-emails}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:21] </span></span> -> [Network Security SMTP](network.md)


#### <span class="section-num">5.19.2</span> [initconf/smtp-url-analysis: Extracting and analyzing URLs from Emails for phishing events](https://github.com/initconf/smtp-url-analysis) {#initconf-smtp-url-analysis-extracting-and-analyzing-urls-from-emails-for-phishing-events}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:26] </span></span> -> [Network Security SMTP](network.md)


## <span class="section-num">6</span> Zeek Plugin or analyzer {#zeek-plugin-or-analyzer}


### <span class="section-num">6.1</span> [J-Gras/zeek-af\_packet-plugin: Plugin providing native AF\_Packet support for Zeek (formerly known as Bro).](https://github.com/J-Gras/zeek-af%5Fpacket-plugin) {#j-gras-zeek-af-packet-plugin-plugin-providing-native-af-packet-support-for-zeek--formerly-known-as-bro--dot}


### <span class="org-todo done DONE">DONE</span> <span class="section-num">6.2</span> [GitHub - reservoirlabs/zeek-zip-analyzer: ZIP analyzer for Zeek](https://github.com/reservoirlabs/zeek-zip-analyzer) {#github-reservoirlabs-zeek-zip-analyzer-zip-analyzer-for-zeek}


### <span class="section-num">6.3</span> [bro-netmap/zkg.meta at master · zeek/bro-netmap · GitHub](https://github.com/zeek/bro-netmap/blob/master/zkg.meta) {#bro-netmap-zkg-dot-meta-at-master-zeek-bro-netmap-github}


### <span class="section-num">6.4</span> [J-Gras/bro-lognorm: Bro plugin providing liblognorm integration.](https://github.com/J-Gras/bro-lognorm) {#j-gras-bro-lognorm-bro-plugin-providing-liblognorm-integration-dot}


### <span class="org-todo done __CANCELED">✘ CANCELED</span> <span class="section-num">6.5</span> [jswaro/tcprs: TCP Retransmission and State Analyzer plugin for the Bro-IDS framework](https://github.com/jswaro/tcprs) {#jswaro-tcprs-tcp-retransmission-and-state-analyzer-plugin-for-the-bro-ids-framework}


### <span class="section-num">6.6</span> [dopheide-esnet/bro-quic: Analyzer that attempts to identify the QUIC protocol.](https://github.com/dopheide-esnet/bro-quic) {#dopheide-esnet-bro-quic-analyzer-that-attempts-to-identify-the-quic-protocol-dot}


## <span class="section-num">7</span> Zeek Threat Intelligence(Intel) {#zeek-threat-intelligence--intel}


### <span class="section-num">7.1</span> [blacklist/scripts at master · initconf/blacklist](https://github.com/initconf/blacklist/tree/master/scripts) {#blacklist-scripts-at-master-initconf-blacklist}

manage blacklisted IP address


### <span class="section-num">7.2</span> [kinomakino/Threat-Intelligence-Data: Snort\_rules detection bad actors.](https://github.com/kinomakino/Threat-Intelligence-Data) {#kinomakino-threat-intelligence-data-snort-rules-detection-bad-actors-dot}


## <span class="section-num">8</span> Zeek Cluster {#zeek-cluster}


### <span class="section-num">8.1</span> [J-Gras/add-node-names: Adds cluster node name to logs.](https://github.com/J-Gras/add-node-names) {#j-gras-add-node-names-adds-cluster-node-name-to-logs-dot}

This package adds the \_node\_name field to Zeek logs to indicate which node generated a log entry. By default the field is only added to the conn.log. For further configuration, the following options are available:


## <span class="section-num">9</span> Zeek Agent {#zeek-agent}


### <span class="section-num">9.1</span> [zeek/zeek-agent: An endpoint monitoring agent that provides host activity to Zeek](https://github.com/zeek/zeek-agent) {#zeek-zeek-agent-an-endpoint-monitoring-agent-that-provides-host-activity-to-zeek}


### <span class="section-num">9.2</span> [zeek/bro-netmap: Native Netmap Packet IOSource for Bro/Zeek](https://github.com/zeek/bro-netmap) {#zeek-bro-netmap-native-netmap-packet-iosource-for-bro-zeek}


### <span class="org-todo done DONE">DONE</span> <span class="section-num">9.3</span> [apache/metron-bro-plugin-kafka: Apache Metron](https://github.com/apache/metron-bro-plugin-kafka) {#apache-metron-bro-plugin-kafka-apache-metron}


### <span class="org-todo done DONE">DONE</span> <span class="section-num">9.4</span> [zeek-postgresql/scripts at master · 0xxon/zeek-postgresql](https://github.com/0xxon/zeek-postgresql/tree/master/scripts) {#zeek-postgresql-scripts-at-master-0xxon-zeek-postgresql}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:10] </span></span> -> [Zeek logs to database](#zeek-logs-to-database)


### <span class="section-num">9.5</span> [ncsa/bro-zeromq-writer: Bro plugin that provides a ZeroMQ log writer.](https://github.com/ncsa/bro-zeromq-writer) {#ncsa-bro-zeromq-writer-bro-plugin-that-provides-a-zeromq-log-writer-dot}


## <span class="section-num">10</span> Zeek Con {#zeek-con}


### <span class="section-num">10.1</span> Virtual ZeekWeek {#virtual-zeekweek}


#### <span class="section-num">10.1.1</span> [Virtual ZeekWeek 2020: Day 3 - YouTube](https://www.youtube.com/watch?v=9ctRt-vfvns&feature=youtu.be) {#virtual-zeekweek-2020-day-3-youtube}


## <span class="section-num">11</span> Zeek ThirdParty Support {#zeek-thirdparty-support}


### <span class="section-num">11.1</span> [joesecurity/Joe-Sandbox-Bro: JoeSandbox-Bro is a simple bro script which extracts files from your internet connection and analyzes them automatically on Joe Sandbox](https://github.com/joesecurity/Joe-Sandbox-Bro) {#joesecurity-joe-sandbox-bro-joesandbox-bro-is-a-simple-bro-script-which-extracts-files-from-your-internet-connection-and-analyzes-them-automatically-on-joe-sandbox}


## <span class="section-num">12</span> Zeek troubleshoot {#zeek-troubleshoot}


### <span class="section-num">12.1</span> [ncsa/bro-doctor](https://github.com/ncsa/bro-doctor) {#ncsa-bro-doctor}


## <span class="section-num">13</span> Zeek deployment {#zeek-deployment}


### <span class="section-num">13.1</span> [ncsa/bro-interface-setup](https://github.com/ncsa/bro-interface-setup) {#ncsa-bro-interface-setup}


## <span class="section-num">14</span> Zeek Notice or alert {#zeek-notice-or-alert}


### <span class="section-num">14.1</span> [pgaulon/zeek-notice-slack: Script extending Zeek Notice framework, adding Slack notifications](https://github.com/pgaulon/zeek-notice-slack) {#pgaulon-zeek-notice-slack-script-extending-zeek-notice-framework-adding-slack-notifications}


## <span class="section-num">15</span> Zeek Lang expression {#zeek-lang-expression}


### <span class="section-num">15.1</span> [Zeek: Zeke on Zeek: Working With Open-Source Zeek: Adding a Key-value For-Loop](https://zeek.org/2019/07/19/zeke-on-zeek-working-with-open-source-zeek-adding-a-key-value-for-loop/) {#zeek-zeke-on-zeek-working-with-open-source-zeek-adding-a-key-value-for-loop}


## <span class="section-num">16</span> Zeek to kafka {#zeek-to-kafka}


### <span class="section-num">16.1</span> [nickwallen’s gists](https://gist.github.com/nickwallen) {#nickwallen-s-gists}
