+++
title = "Network monitoring"
lastmod = 2020-11-22T16:46:07-08:00
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

- <span class="section-num">1</span> [hardware](#hardware)
    - <span class="section-num">1.1</span> [AnalogJ/scrutiny: Hard Drive S.M.A.R.T Monitoring, Historical Trends & Real World Failure Thresholds](#analogj-scrutiny-hard-drive-s-dot-m-dot-a-dot-r-dot-t-monitoring-historical-trends-and-real-world-failure-thresholds)
- <span class="section-num">2</span> [DNS](#dns)
    - <span class="section-num">2.1</span> [StackExchange/dnscontrol: Synchronize your DNS to multiple providers from a simple DSL](#stackexchange-dnscontrol-synchronize-your-dns-to-multiple-providers-from-a-simple-dsl)
- <span class="section-num">3</span> [timeline analysis](#timeline-analysis)
    - <span class="section-num">3.1</span> [GitHub - google/timesketch: Collaborative forensic timeline analysis](#github-google-timesketch-collaborative-forensic-timeline-analysis)
- <span class="section-num">4</span> [NSM project](#nsm-project)
    - <span class="section-num">4.1</span> [<span class="org-todo todo TODO">TODO</span> HASecuritySolutions/VulnWhisperer: Create actionable data from your Vulnerability Scans](#hasecuritysolutions-vulnwhisperer-create-actionable-data-from-your-vulnerability-scans):learn:
    - <span class="section-num">4.2</span> [dynamite-sdk-lite/working\_with\_events.ipynb at master · DynamiteAI/dynamite-sdk-lite](#dynamite-sdk-lite-working-with-events-dot-ipynb-at-master-dynamiteai-dynamite-sdk-lite)
    - <span class="section-num">4.3</span> [<span class="org-todo todo TODO">TODO</span> bettercap/bettercap: The Swiss Army knife for 802.11, BLE and Ethernet networks reconnaissance and MITM attacks.](#bettercap-bettercap-the-swiss-army-knife-for-802-dot-11-ble-and-ethernet-networks-reconnaissance-and-mitm-attacks-dot)
    - <span class="section-num">4.4</span> [WiproOpenSource/galaxia: Next Generation Universal monitoring framework for infrastructure, applications & microservices](#wiproopensource-galaxia-next-generation-universal-monitoring-framework-for-infrastructure-applications-and-microservices)
- <span class="section-num">5</span> [Network protocol analyzer](#network-protocol-analyzer)
    - <span class="section-num">5.1</span> [Wireshark · Go Deep.](#wireshark-go-deep-dot)
    - <span class="section-num">5.2</span> [brimsec/brim: Desktop application to efficiently search large packet captures and Zeek logs.](#brimsec-brim-desktop-application-to-efficiently-search-large-packet-captures-and-zeek-logs-dot)
- <span class="section-num">6</span> [Red Team](#red-team)
    - <span class="section-num">6.1</span> [OpenCSPM/opencspm: Open Cloud Security Posture Management Engine](#opencspm-opencspm-open-cloud-security-posture-management-engine)
- <span class="section-num">7</span> [time](#time)
    - <span class="section-num">7.1</span> [Switching from Log2Timeline Perl (Legacy) to Plaso — Plaso (log2timeline) 20201007 documentation](#switching-from-log2timeline-perl--legacy--to-plaso-plaso--log2timeline--20201007-documentation)
- <span class="section-num">8</span> [NSM ELK Project](#nsm-elk-project)
    - <span class="section-num">8.1</span> [StamusNetworks/SELKS: A Suricata based IDS/IPS distro](#stamusnetworks-selks-a-suricata-based-ids-ips-distro)
    - <span class="section-num">8.2</span> [philhagen/sof-elk: Configuration files for the SOF-ELK VM, used in SANS FOR572](#philhagen-sof-elk-configuration-files-for-the-sof-elk-vm-used-in-sans-for572)
    - <span class="section-num">8.3</span> [austin-taylor/flare: An analytical framework for network traffic and behavioral analytics](#austin-taylor-flare-an-analytical-framework-for-network-traffic-and-behavioral-analytics)
- <span class="section-num">9</span> [The Security Onion Cloud Client Network Security Monitoring for the Cloud](#the-security-onion-cloud-client-network-security-monitoring-for-the-cloud)
- <span class="section-num">10</span> [NSM data analysis](#nsm-data-analysis)
    - <span class="section-num">10.1</span> [Jupyter Notebooks 📓 from SIGMA Rules 🛡⚔️ to Query Elasticsearch 🏹 | by Roberto Rodriguez | Open Threat Research | Medium](#jupyter-notebooks-from-sigma-rules-️-to-query-elasticsearch-by-roberto-rodriguez-open-threat-research-medium)
    - <span class="section-num">10.2</span> [lbnl-cybersecurity/tstat-dtn-analysis: prediction tools for tstat data](#lbnl-cybersecurity-tstat-dtn-analysis-prediction-tools-for-tstat-data)
- <span class="section-num">11</span> [Threat Intelligence](#threat-intelligence)
    - <span class="section-num">11.1</span> [P3t3rp4rk3r/Threat\_Intelligence: Threat-Intelligence Feeds & Tools & Frameworks](#p3t3rp4rk3r-threat-intelligence-threat-intelligence-feeds-and-tools-and-frameworks)
- <span class="section-num">12</span> [Windows Sysmon](#windows-sysmon)
    - <span class="section-num">12.1</span> [https://github.com/SwiftOnSecurity/sysmon-config](#https-github-dot-com-swiftonsecurity-sysmon-config)
    - <span class="section-num">12.2</span> [https://github.com/JPCERTCC/SysmonSearch](#https-github-dot-com-jpcertcc-sysmonsearch)

</div>
<!--endtoc-->



## <span class="section-num">1</span> hardware {#hardware}


### <span class="section-num">1.1</span> [AnalogJ/scrutiny: Hard Drive S.M.A.R.T Monitoring, Historical Trends & Real World Failure Thresholds](https://github.com/AnalogJ/scrutiny) {#analogj-scrutiny-hard-drive-s-dot-m-dot-a-dot-r-dot-t-monitoring-historical-trends-and-real-world-failure-thresholds}


## <span class="section-num">2</span> DNS {#dns}


### <span class="section-num">2.1</span> [StackExchange/dnscontrol: Synchronize your DNS to multiple providers from a simple DSL](https://github.com/StackExchange/dnscontrol) {#stackexchange-dnscontrol-synchronize-your-dns-to-multiple-providers-from-a-simple-dsl}


## <span class="section-num">3</span> timeline analysis {#timeline-analysis}


### <span class="section-num">3.1</span> [GitHub - google/timesketch: Collaborative forensic timeline analysis](https://github.com/google/timesketch) {#github-google-timesketch-collaborative-forensic-timeline-analysis}


## <span class="section-num">4</span> NSM project {#nsm-project}


### <span class="org-todo todo TODO">TODO</span> <span class="section-num">4.1</span> [HASecuritySolutions/VulnWhisperer: Create actionable data from your Vulnerability Scans](https://github.com/HASecuritySolutions/VulnWhisperer) {#hasecuritysolutions-vulnwhisperer-create-actionable-data-from-your-vulnerability-scans}


### <span class="section-num">4.2</span> [dynamite-sdk-lite/working\_with\_events.ipynb at master · DynamiteAI/dynamite-sdk-lite](https://github.com/DynamiteAI/dynamite-sdk-lite/blob/master/notebooks/getting%5Fstarted/working%5Fwith%5Fevents.ipynb) {#dynamite-sdk-lite-working-with-events-dot-ipynb-at-master-dynamiteai-dynamite-sdk-lite}


### <span class="org-todo todo TODO">TODO</span> <span class="section-num">4.3</span> [bettercap/bettercap: The Swiss Army knife for 802.11, BLE and Ethernet networks reconnaissance and MITM attacks.](https://github.com/bettercap/bettercap) {#bettercap-bettercap-the-swiss-army-knife-for-802-dot-11-ble-and-ethernet-networks-reconnaissance-and-mitm-attacks-dot}


### <span class="section-num">4.4</span> [WiproOpenSource/galaxia: Next Generation Universal monitoring framework for infrastructure, applications & microservices](https://github.com/WiproOpenSource/galaxia) {#wiproopensource-galaxia-next-generation-universal-monitoring-framework-for-infrastructure-applications-and-microservices}


## <span class="section-num">5</span> Network protocol analyzer {#network-protocol-analyzer}


### <span class="section-num">5.1</span> [Wireshark · Go Deep.](https://www.wireshark.org/) {#wireshark-go-deep-dot}


### <span class="section-num">5.2</span> [brimsec/brim: Desktop application to efficiently search large packet captures and Zeek logs.](https://github.com/brimsec/brim) {#brimsec-brim-desktop-application-to-efficiently-search-large-packet-captures-and-zeek-logs-dot}

-   [Awesome Zeek]({{< relref "awesome-zeek" >}})


## <span class="section-num">6</span> Red Team {#red-team}


### <span class="section-num">6.1</span> [OpenCSPM/opencspm: Open Cloud Security Posture Management Engine](https://github.com/OpenCSPM/opencspm) {#opencspm-opencspm-open-cloud-security-posture-management-engine}


## <span class="section-num">7</span> time {#time}


### <span class="section-num">7.1</span> [Switching from Log2Timeline Perl (Legacy) to Plaso — Plaso (log2timeline) 20201007 documentation](https://plaso.readthedocs.io/en/latest/sources/user/Log2Timeline-Perl-%28Legacy%29.html#new-method) {#switching-from-log2timeline-perl--legacy--to-plaso-plaso--log2timeline--20201007-documentation}


## <span class="section-num">8</span> NSM ELK Project {#nsm-elk-project}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 16:23] </span></span> <- [Elk security platforms](elk.md)


### <span class="section-num">8.1</span> [StamusNetworks/SELKS: A Suricata based IDS/IPS distro](https://github.com/StamusNetworks/SELKS) {#stamusnetworks-selks-a-suricata-based-ids-ips-distro}


### <span class="section-num">8.2</span> [philhagen/sof-elk: Configuration files for the SOF-ELK VM, used in SANS FOR572](https://github.com/philhagen/sof-elk) {#philhagen-sof-elk-configuration-files-for-the-sof-elk-vm-used-in-sans-for572}


### <span class="section-num">8.3</span> [austin-taylor/flare: An analytical framework for network traffic and behavioral analytics](https://github.com/austin-taylor/flare) {#austin-taylor-flare-an-analytical-framework-for-network-traffic-and-behavioral-analytics}


## <span class="section-num">9</span> [The Security Onion Cloud Client Network Security Monitoring for the Cloud](https://www.sans.org/reading-room/whitepapers/cloud/security-onion-cloud-client-network-security-monitoring-cloud-34335) {#the-security-onion-cloud-client-network-security-monitoring-for-the-cloud}


## <span class="section-num">10</span> NSM data analysis {#nsm-data-analysis}


### <span class="section-num">10.1</span> [Jupyter Notebooks 📓 from SIGMA Rules 🛡⚔️ to Query Elasticsearch 🏹 | by Roberto Rodriguez | Open Threat Research | Medium](https://medium.com/threat-hunters-forge/jupyter-notebooks-from-sigma-rules-%EF%B8%8F-to-query-elasticsearch-31a74cc59b99) {#jupyter-notebooks-from-sigma-rules-️-to-query-elasticsearch-by-roberto-rodriguez-open-threat-research-medium}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 16:02] </span></span> -> [GTrunSec/Jupyter-data-science-environment: Including Haskell, R, Julia,Python and Jupyter Kernels generated by Nix](Jupyter-data-science.md)


### <span class="section-num">10.2</span> [lbnl-cybersecurity/tstat-dtn-analysis: prediction tools for tstat data](https://github.com/lbnl-cybersecurity/tstat-dtn-analysis) {#lbnl-cybersecurity-tstat-dtn-analysis-prediction-tools-for-tstat-data}


## <span class="section-num">11</span> Threat Intelligence {#threat-intelligence}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 16:13] </span></span> -> [zeek Intel feed](awesome-zeek.md)


### <span class="section-num">11.1</span> [P3t3rp4rk3r/Threat\_Intelligence: Threat-Intelligence Feeds & Tools & Frameworks](https://github.com/P3t3rp4rk3r/Threat%5FIntelligence) {#p3t3rp4rk3r-threat-intelligence-threat-intelligence-feeds-and-tools-and-frameworks}


## <span class="section-num">12</span> Windows Sysmon {#windows-sysmon}


### <span class="section-num">12.1</span> <https://github.com/SwiftOnSecurity/sysmon-config> {#https-github-dot-com-swiftonsecurity-sysmon-config}


### <span class="section-num">12.2</span> <https://github.com/JPCERTCC/SysmonSearch> {#https-github-dot-com-jpcertcc-sysmonsearch}
