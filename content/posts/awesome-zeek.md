+++
title = "Awesome Zeek"
lastmod = 2020-10-16T13:59:25-07:00
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
    - <span class="section-num">5.2</span> [ZeeK Script DNS<code>[0/0]</code>](#zeek-script-dns)
        - <span class="section-num">5.2.1</span> [<span class="org-todo done DONE">DONE</span> [ ] [] https://github.com/hhzzk/dns-tunnels](#https-github-dot-com-hhzzk-dns-tunnels):DNS:
        - <span class="section-num">5.2.2</span> [<span class="org-todo done DONE">DONE</span> [ ][dns axfr query ] https://github.com/srozb/dns\_axfr](#dns-axfr-query-https-github-dot-com-srozb-dns-axfr):DNS:
        - <span class="section-num">5.2.3</span> [<span class="org-todo done DONE">DONE</span> https://github.com/corelight/top-dns](#https-github-dot-com-corelight-top-dns):LEARN:Necessary:
    - <span class="section-num">5.3</span> [Zeek Script Conn<code>[3/3]</code>](#zeek-script-conn)
        - <span class="section-num">5.3.1</span> [<span class="org-todo done DONE">DONE</span> [Long Connections] https://github.com/corelight/bro-long-connections](#long-connections-https-github-dot-com-corelight-bro-long-connections):Necessary:
        - <span class="section-num">5.3.2</span> [<span class="org-todo done DONE">DONE</span> [Connection Burst Identification] https://github.com/corelight/conn-burst](#connection-burst-identification-https-github-dot-com-corelight-conn-burst):Necessary:
        - <span class="section-num">5.3.3</span> [[SMB] https://www.giac.org/paper/gcia/10091/detecting-malicious-smb-activity-bro/140938](#smb-https-www-dot-giac-dot-org-paper-gcia-10091-detecting-malicious-smb-activity-bro-140938)
        - <span class="section-num">5.3.4</span> [<span class="org-todo done __CANCELED">✘ CANCELED</span> [Extended TCP Analysis] https://github.com/jswaro/tcprs](#extended-tcp-analysis-https-github-dot-com-jswaro-tcprs)
    - <span class="section-num">5.4</span> [Zeek Script logging <code>[2/7]</code>](#zeek-script-logging)
    - <span class="section-num">5.5</span> [Zeek CVE Detection](#zeek-cve-detection)
        - <span class="section-num">5.5.1</span> [GitHub - corelight/CVE-2020-16898: A network detection package for CVE-2020-16898 (Windows TCP/IP Remote Code Execution Vulnerability)](#github-corelight-cve-2020-16898-a-network-detection-package-for-cve-2020-16898--windows-tcp-ip-remote-code-execution-vulnerability):windows:
        - <span class="section-num">5.5.2</span> [GitHub - 0xxon/cve-2020-0601: Zeek package to detect CVE-2020-0601](#github-0xxon-cve-2020-0601-zeek-package-to-detect-cve-2020-0601)
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

-   [Slack | general | Zeek | 1 new item](https://app.slack.com/client/TSXGCHZE1/CSZBXF6TH)


## <span class="section-num">1</span> Zeek installation {#zeek-installation}


### <span class="section-num">1.1</span> [Zeekurity Zen - Part I: How to Install Zeek on CentOS 8 - ericooi.com](https://www.ericooi.com/zeekurity-zen-part-i-how-to-install-zeek-on-centos-8/#comment-1670) {#zeekurity-zen-part-i-how-to-install-zeek-on-centos-8-ericooi-dot-com}


#### <span class="section-num">1.1.1</span> [Zeekurity Zen Zeries - ericooi.com](https://www.ericooi.com/zeekurity-zen-zeries/) {#zeekurity-zen-zeries-ericooi-dot-com}


## <span class="section-num">2</span> Zeek Documents {#zeek-documents}


### <span class="section-num">2.1</span> Zeek logging {#zeek-logging}


#### <span class="section-num">2.1.1</span> [Logging — Zeek User Manual v3.2.2](https://docs.zeek.org/en/current/examples/logs/) {#logging-zeek-user-manual-v3-dot-2-dot-2}

<span class="timestamp-wrapper"><span class="timestamp">[2020-10-14 Wed 23:50] </span></span> <- [Using zeek-cut with logs](#using-zeek-cut-with-logs)


#### <span class="section-num">2.1.2</span> [2019-04-cern-zeek-logging.pdf](https://indico.cern.ch/event/762505/contributions/3375201/attachments/1830709/2998002/2019-04-cern-zeek-logging.pdf) {#2019-04-cern-zeek-logging-dot-pdf}


## <span class="section-num">3</span> Zeek-cut {#zeek-cut}


### <span class="section-num">3.1</span> Using zeek-cut with logs {#using-zeek-cut-with-logs}

-   [Logging — Zeek User Manual v3.2.2](#logging-zeek-user-manual-v3-dot-2-dot-2)


## <span class="section-num">4</span> Zeek Performance {#zeek-performance}


### <span class="section-num">4.1</span> [mozilla/zept: Zeek Extreme Performance Tuning](https://github.com/mozilla/zept) {#mozilla-zept-zeek-extreme-performance-tuning}

\*


## <span class="section-num">5</span> Zeek Script {#zeek-script}


### <span class="section-num">5.1</span> Zeek Script Documents {#zeek-script-documents}


#### <span class="section-num">5.1.1</span> [Give me my stats!](https://corelight.blog/2020/09/21/give-me-my-stats/) {#give-me-my-stats}


### <span class="section-num">5.2</span> ZeeK Script DNS<code>[0/0]</code> {#zeek-script-dns}


#### <span class="org-todo done DONE">DONE</span> <span class="section-num">5.2.1</span> [ ] [] <https://github.com/hhzzk/dns-tunnels> {#https-github-dot-com-hhzzk-dns-tunnels}


#### <span class="org-todo done DONE">DONE</span> <span class="section-num">5.2.2</span> [ ][dns axfr query ] <https://github.com/srozb/dns%5Faxfr> {#dns-axfr-query-https-github-dot-com-srozb-dns-axfr}

<!--list-separator-->

1.  <https://en.wikipedia.org/wiki/DNS%5Fzone%5Ftransfer>

<!--list-separator-->

2.  <https://cr.yp.to/djbdns/axfr-notes.html>


#### <span class="org-todo done DONE">DONE</span> <span class="section-num">5.2.3</span> <https://github.com/corelight/top-dns> {#https-github-dot-com-corelight-top-dns}

-   State "DONE"     from              <span class="timestamp-wrapper"><span class="timestamp">[2019-08-10 Sat 21:11]</span></span>


### <span class="section-num">5.3</span> Zeek Script Conn<code>[3/3]</code> {#zeek-script-conn}


#### <span class="org-todo done DONE">DONE</span> <span class="section-num">5.3.1</span> [Long Connections] <https://github.com/corelight/bro-long-connections> {#long-connections-https-github-dot-com-corelight-bro-long-connections}


#### <span class="org-todo done DONE">DONE</span> <span class="section-num">5.3.2</span> [Connection Burst Identification] <https://github.com/corelight/conn-burst> {#connection-burst-identification-https-github-dot-com-corelight-conn-burst}


#### <span class="section-num">5.3.3</span> [SMB] <https://www.giac.org/paper/gcia/10091/detecting-malicious-smb-activity-bro/140938> {#smb-https-www-dot-giac-dot-org-paper-gcia-10091-detecting-malicious-smb-activity-bro-140938}


#### <span class="org-todo done __CANCELED">✘ CANCELED</span> <span class="section-num">5.3.4</span> [Extended TCP Analysis] <https://github.com/jswaro/tcprs> {#extended-tcp-analysis-https-github-dot-com-jswaro-tcprs}

[SMBv1] <https://github.com/klehigh/find%5Fsmbv1>


### <span class="section-num">5.4</span> Zeek Script logging <code>[2/7]</code> {#zeek-script-logging}

-   [X] [Vlan tags] <https://github.com/corelight/log-add-vlan-everywhere>
    [filter] <https://github.com/hosom/log-filters>
    [json]  <https://github.com/J-Gras/add-json>
    [] <https://github.com/corelight/json-streaming-logs>
    [liblognorm] <https://github.com/J-Gras/bro-lognorm>
    [AF\_packet] <https://github.com/J-Gras/bro-af%5Fpacket-plugin>

<!--listend-->

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


### <span class="section-num">5.5</span> Zeek CVE Detection {#zeek-cve-detection}


#### <span class="section-num">5.5.1</span> [GitHub - corelight/CVE-2020-16898: A network detection package for CVE-2020-16898 (Windows TCP/IP Remote Code Execution Vulnerability)](https://github.com/corelight/CVE-2020-16898) {#github-corelight-cve-2020-16898-a-network-detection-package-for-cve-2020-16898--windows-tcp-ip-remote-code-execution-vulnerability}


#### <span class="section-num">5.5.2</span> [GitHub - 0xxon/cve-2020-0601: Zeek package to detect CVE-2020-0601](https://github.com/0xxon/cve-2020-0601) {#github-0xxon-cve-2020-0601-zeek-package-to-detect-cve-2020-0601}


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
