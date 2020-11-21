+++
title = "Awesome Zeek"
lastmod = 2020-11-21T03:17:28-08:00
draft = false
creator = "Emacs 28.0.50 (Org mode 9.4 + ox-hugo)"
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
        - <span class="section-num">5.4.3</span> [[SMB] https://www.giac.org/paper/gcia/10091/detecting-malicious-smb-activity-bro/140938](#smb-https-www-dot-giac-dot-org-paper-gcia-10091-detecting-malicious-smb-activity-bro-140938)
        - <span class="section-num">5.4.4</span> [<span class="org-todo done __CANCELED">✘ CANCELED</span> [Extended TCP Analysis] https://github.com/jswaro/tcprs](#extended-tcp-analysis-https-github-dot-com-jswaro-tcprs)
    - <span class="section-num">5.5</span> [Zeek Script logging <code>[2/7]</code>](#zeek-script-logging)
    - <span class="section-num">5.6</span> [Zeel Vlan](#zeel-vlan)
        - <span class="section-num">5.6.1</span> [https://github.com/corelight/log-add-vlan-everywhere](#https-github-dot-com-corelight-log-add-vlan-everywhere)
    - <span class="section-num">5.7</span> [Zeek CVE Detection](#zeek-cve-detection)
        - <span class="section-num">5.7.1</span> [GitHub - corelight/CVE-2020-16898: A network detection package for CVE-2020-16898 (Windows TCP/IP Remote Code Execution Vulnerability)](#github-corelight-cve-2020-16898-a-network-detection-package-for-cve-2020-16898--windows-tcp-ip-remote-code-execution-vulnerability):windows:
        - <span class="section-num">5.7.2</span> [GitHub - 0xxon/cve-2020-0601: Zeek package to detect CVE-2020-0601](#github-0xxon-cve-2020-0601-zeek-package-to-detect-cve-2020-0601)
- <span class="section-num">6</span> [Zeek Plugin or analyzer](#zeek-plugin-or-analyzer)
    - <span class="section-num">6.1</span> [<span class="org-todo done DONE">DONE</span> GitHub - reservoirlabs/zeek-zip-analyzer: ZIP analyzer for Zeek](#github-reservoirlabs-zeek-zip-analyzer-zip-analyzer-for-zeek):analyzer:
    - <span class="section-num">6.2</span> [bro-netmap/zkg.meta at master · zeek/bro-netmap · GitHub](#bro-netmap-zkg-dot-meta-at-master-zeek-bro-netmap-github):packet:
- <span class="section-num">7</span> [Zeek Agent](#zeek-agent)
    - <span class="section-num">7.1</span> [<span class="org-todo done DONE">DONE</span> https://github.com/apache/metron-bro-plugin-kafka](#https-github-dot-com-apache-metron-bro-plugin-kafka):agent:
    - <span class="section-num">7.2</span> [<span class="org-todo done DONE">DONE</span> zeek-postgresql/scripts at master · 0xxon/zeek-postgresql](#zeek-postgresql-scripts-at-master-0xxon-zeek-postgresql):agent:
- <span class="section-num">8</span> [Zeek Con](#zeek-con)
    - <span class="section-num">8.1</span> [Virtual ZeekWeek](#virtual-zeekweek)
        - <span class="section-num">8.1.1</span> [day3](#day3)

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


#### <span class="section-num">2.1.1</span> [Logging — Zeek User Manual v3.2.2](https://docs.zeek.org/en/current/examples/logs/) {#logging-zeek-user-manual-v3-dot-2-dot-2}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-10-14 Wed 23:50] </span></span> <- [Using zeek-cut with logs](#using-zeek-cut-with-logs)


#### <span class="section-num">2.1.2</span> [2019-04-cern-zeek-logging.pdf](https://indico.cern.ch/event/762505/contributions/3375201/attachments/1830709/2998002/2019-04-cern-zeek-logging.pdf) {#2019-04-cern-zeek-logging-dot-pdf}


## <span class="section-num">3</span> Zeek-cut {#zeek-cut}


### <span class="section-num">3.1</span> Using zeek-cut with logs {#using-zeek-cut-with-logs}

-   [Logging — Zeek User Manual v3.2.2](#logging-zeek-user-manual-v3-dot-2-dot-2)


## <span class="section-num">4</span> Zeek Performance {#zeek-performance}


### <span class="section-num">4.1</span> [mozilla/zept: Zeek Extreme Performance Tuning](https://github.com/mozilla/zept) {#mozilla-zept-zeek-extreme-performance-tuning}


## <span class="section-num">5</span> Zeek Script {#zeek-script}


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


#### <span class="section-num">5.4.3</span> [SMB] <https://www.giac.org/paper/gcia/10091/detecting-malicious-smb-activity-bro/140938> {#smb-https-www-dot-giac-dot-org-paper-gcia-10091-detecting-malicious-smb-activity-bro-140938}


#### <span class="org-todo done __CANCELED">✘ CANCELED</span> <span class="section-num">5.4.4</span> [Extended TCP Analysis] <https://github.com/jswaro/tcprs> {#extended-tcp-analysis-https-github-dot-com-jswaro-tcprs}

[SMBv1] <https://github.com/klehigh/find%5Fsmbv1>


### <span class="section-num">5.5</span> Zeek Script logging <code>[2/7]</code> {#zeek-script-logging}

[filter] <https://github.com/hosom/log-filters>
[json]  <https://github.com/J-Gras/add-json>
[] <https://github.com/corelight/json-streaming-logs>
[liblognorm] <https://github.com/J-Gras/bro-lognorm>
[AF\_packet] <https://github.com/J-Gras/bro-af%5Fpacket-plugin>

-   [ ] [database

<!--listend-->

```sh
sudo -u postgres psql
sudo -u postgres createuser <username>
 sudo -u postgres createdb <dbname>
createdb -h localhost -p 5432 -U dbuser testdb
psql -h localhost -p 5432 -U dbuser -d testdb
```

-   [Creating user, database and adding access on PostgreSQL](https://medium.com/coding-blocks/creating-user-database-and-adding-access-on-postgresql-8bfcd2f4a91e)

<!--listend-->

-   [ ] [json-jq] [Working with JSON in bash using jq - Cameron Nokes](https://cameronnokes.com/blog/working-with-json-in-bash-using-jq/)


### <span class="section-num">5.6</span> Zeel Vlan {#zeel-vlan}


#### <span class="section-num">5.6.1</span> <https://github.com/corelight/log-add-vlan-everywhere> {#https-github-dot-com-corelight-log-add-vlan-everywhere}


### <span class="section-num">5.7</span> Zeek CVE Detection {#zeek-cve-detection}


#### <span class="section-num">5.7.1</span> [GitHub - corelight/CVE-2020-16898: A network detection package for CVE-2020-16898 (Windows TCP/IP Remote Code Execution Vulnerability)](https://github.com/corelight/CVE-2020-16898) {#github-corelight-cve-2020-16898-a-network-detection-package-for-cve-2020-16898--windows-tcp-ip-remote-code-execution-vulnerability}


#### <span class="section-num">5.7.2</span> [GitHub - 0xxon/cve-2020-0601: Zeek package to detect CVE-2020-0601](https://github.com/0xxon/cve-2020-0601) {#github-0xxon-cve-2020-0601-zeek-package-to-detect-cve-2020-0601}


## <span class="section-num">6</span> Zeek Plugin or analyzer {#zeek-plugin-or-analyzer}


### <span class="org-todo done DONE">DONE</span> <span class="section-num">6.1</span> [GitHub - reservoirlabs/zeek-zip-analyzer: ZIP analyzer for Zeek](https://github.com/reservoirlabs/zeek-zip-analyzer) {#github-reservoirlabs-zeek-zip-analyzer-zip-analyzer-for-zeek}


### <span class="section-num">6.2</span> [bro-netmap/zkg.meta at master · zeek/bro-netmap · GitHub](https://github.com/zeek/bro-netmap/blob/master/zkg.meta) {#bro-netmap-zkg-dot-meta-at-master-zeek-bro-netmap-github}


## <span class="section-num">7</span> Zeek Agent {#zeek-agent}


### <span class="org-todo done DONE">DONE</span> <span class="section-num">7.1</span> <https://github.com/apache/metron-bro-plugin-kafka> {#https-github-dot-com-apache-metron-bro-plugin-kafka}


### <span class="org-todo done DONE">DONE</span> <span class="section-num">7.2</span> [zeek-postgresql/scripts at master · 0xxon/zeek-postgresql](https://github.com/0xxon/zeek-postgresql/tree/master/scripts) {#zeek-postgresql-scripts-at-master-0xxon-zeek-postgresql}


## <span class="section-num">8</span> Zeek Con {#zeek-con}


### <span class="section-num">8.1</span> Virtual ZeekWeek {#virtual-zeekweek}


#### <span class="section-num">8.1.1</span> day3 {#day3}

-   [https://www.youtube.com/watch?v=9ctRt-vfvns&feature=youtu.be](https://www.youtube.com/watch?v=9ctRt-vfvns&feature=youtu.be)
