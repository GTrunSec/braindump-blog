+++
title = "Elastic"
lastmod = 2020-11-22T17:03:49-08:00
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

- <span class="section-num">1</span> [ELK Security Platforms](#elk-security-platforms)
    - <span class="section-num">1.1</span> [maliceio/malice: VirusTotal Wanna Be - Now with 100% more Hipster](#maliceio-malice-virustotal-wanna-be-now-with-100-more-hipster)
    - <span class="section-num">1.2</span> [EvtxToElk - 自动化分析 Windows 事件日志的 python 模块:](#evtxtoelk-自动化分析-windows-事件日志的-python-模块):windows:
- <span class="section-num">2</span> [ELK Tools](#elk-tools)
    - <span class="section-num">2.1</span> [elasticsearch-dump/elasticsearch-dump: Import and export tools for elasticsearch](#elasticsearch-dump-elasticsearch-dump-import-and-export-tools-for-elasticsearch)
    - <span class="section-num">2.2</span> [medcl/elasticsearch-proxy: A lightweight elasticsearch proxy written in golang](#medcl-elasticsearch-proxy-a-lightweight-elasticsearch-proxy-written-in-golang)
- <span class="section-num">3</span> [ELK Alert](#elk-alert)
    - <span class="section-num">3.1</span> [fmorningconsult/go-elasticsearch-alerts: Elasticsearch Alerting Daemon](#fmorningconsult-go-elasticsearch-alerts-elasticsearch-alerting-daemon)
- <span class="section-num">4</span> [ELK GEOIP](#elk-geoip)
    - <span class="section-num">4.1</span> [GEOIP<span class="timestamp-wrapper"><span class="timestamp">&lt;2018-06-14 Thu&gt;</span></span>](#geoip)
    - <span class="section-num">4.2</span> [<span class="org-todo done DONE">DONE</span> "No handler for type [string] declared on field [test]" after update to ES6 · Issue #804 · elastic/elasticsearch-dsl-py](#no-handler-for-type-string-declared-on-field-test-after-update-to-es6-issue-804-elastic-elasticsearch-dsl-py):GEOIP:
- <span class="section-num">5</span> [ELK conf](#elk-conf)
    - <span class="section-num">5.1</span> [ELKSecurity/csv.conf at master · anelshaer/ELKSecurity](#elksecurity-csv-dot-conf-at-master-anelshaer-elksecurity)
    - <span class="section-num">5.2</span> [HASecuritySolutions/Logstash: Contains Logstash related content including tons of Logstash configurations](#hasecuritysolutions-logstash-contains-logstash-related-content-including-tons-of-logstash-configurations)

</div>
<!--endtoc-->



## <span class="section-num">1</span> ELK Security Platforms {#elk-security-platforms}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 17:03] </span></span> <- [HASecuritySolutions/Logstash: Contains Logstash related content including tons of Logstash configurations](#hasecuritysolutions-logstash-contains-logstash-related-content-including-tons-of-logstash-configurations)
-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 16:24] </span></span> <- [NSM ELK Project](nsm.md)


### <span class="section-num">1.1</span> [maliceio/malice: VirusTotal Wanna Be - Now with 100% more Hipster](https://github.com/maliceio/malice) {#maliceio-malice-virustotal-wanna-be-now-with-100-more-hipster}


### <span class="section-num">1.2</span> EvtxToElk - 自动化分析 Windows 事件日志的 python 模块: {#evtxtoelk-自动化分析-windows-事件日志的-python-模块}

<https://dragos.com/blog/20180717EvtxToElk.html>


## <span class="section-num">2</span> ELK Tools {#elk-tools}


### <span class="section-num">2.1</span> [elasticsearch-dump/elasticsearch-dump: Import and export tools for elasticsearch](https://github.com/elasticsearch-dump/elasticsearch-dump) {#elasticsearch-dump-elasticsearch-dump-import-and-export-tools-for-elasticsearch}


### <span class="section-num">2.2</span> [medcl/elasticsearch-proxy: A lightweight elasticsearch proxy written in golang](https://github.com/medcl/elasticsearch-proxy) {#medcl-elasticsearch-proxy-a-lightweight-elasticsearch-proxy-written-in-golang}


## <span class="section-num">3</span> ELK Alert {#elk-alert}


### <span class="section-num">3.1</span> [fmorningconsult/go-elasticsearch-alerts: Elasticsearch Alerting Daemon](https://github.com/morningconsult/go-elasticsearch-alerts) {#fmorningconsult-go-elasticsearch-alerts-elasticsearch-alerting-daemon}

-   [My Golang]({{< relref "my-golang" >}})


## <span class="section-num">4</span> ELK GEOIP {#elk-geoip}


### <span class="section-num">4.1</span> GEOIP<span class="timestamp-wrapper"><span class="timestamp">&lt;2018-06-14 Thu&gt;</span></span> {#geoip}


### <span class="org-todo done DONE">DONE</span> <span class="section-num">4.2</span> ["No handler for type [string] declared on field [test]" after update to ES6 · Issue #804 · elastic/elasticsearch-dsl-py](https://github.com/elastic/elasticsearch-dsl-py/issues/804) {#no-handler-for-type-string-declared-on-field-test-after-update-to-es6-issue-804-elastic-elasticsearch-dsl-py}

CLOSED: <span class="timestamp-wrapper"><span class="timestamp">[2018-06-14 Thu 15:01]</span></span>

-   State "DONE"       from              <span class="timestamp-wrapper"><span class="timestamp">[2018-06-14 Thu 13:39]</span></span>

-   curl -H "Content-Type: application/json" -XPOST localhost:9200/us-city/city/ -d '{"city": "Anchorage", "state": "AK","location": {"lat": "61.2180556", "lon": "-149.9002778"}}'

<!--listend-->

-   <https://www.elastic.co/blog/strict-content-type-checking-for-elasticsearch-rest-requests>

<!--listend-->

-   <http://www.elasticsearchtutorial.com/spatial-search-tutorial.html>


## <span class="section-num">5</span> ELK conf {#elk-conf}


### <span class="section-num">5.1</span> [ELKSecurity/csv.conf at master · anelshaer/ELKSecurity](https://github.com/anelshaer/ELKSecurity/blob/master/logstash/conf.d/csv.conf) {#elksecurity-csv-dot-conf-at-master-anelshaer-elksecurity}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 16:35] </span></span> -> [ELK Security Platforms](#elk-security-platforms)


### <span class="section-num">5.2</span> [HASecuritySolutions/Logstash: Contains Logstash related content including tons of Logstash configurations](https://github.com/HASecuritySolutions/Logstash) {#hasecuritysolutions-logstash-contains-logstash-related-content-including-tons-of-logstash-configurations}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 17:03] </span></span> -> [ELK Security Platforms](#elk-security-platforms)
