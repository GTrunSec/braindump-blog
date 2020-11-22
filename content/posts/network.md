+++
title = "Network"
lastmod = 2020-11-22T03:50:26-08:00
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

- <span class="section-num">1</span> [Network DNS](#network-dns)
    - <span class="section-num">1.1</span> [ogham/dog: Command-line DNS client](#ogham-dog-command-line-dns-client)
    - <span class="section-num">1.2</span> [GitHub - pymumu/smartdns: A local DNS server to obtain the fastest website IP for the best Internet experience， 一个本地DNS服务器，获取最快的网站IP，获得最佳上网体验。](#github-pymumu-smartdns-a-local-dns-server-to-obtain-the-fastest-website-ip-for-the-best-internet-experience-一个本地dns服务器-获取最快的网站ip-获得最佳上网体验)
    - <span class="section-num">1.3</span> [DNS Script](#dns-script)
        - <span class="section-num">1.3.1</span> [Quickpost: nslookup Types | Didier Stevens](#quickpost-nslookup-types-didier-stevens)
    - <span class="section-num">1.4</span> [Network Security Project or Idea DNS](#network-security-project-or-idea--security-dot-md--dns)
        - <span class="section-num">1.4.1</span> [detecting-dns-tunneling](#detecting-dns-tunneling)
- <span class="section-num">2</span> [Network Protocol](#network-protocol)
- <span class="section-num">3</span> [Network SSL](#network-ssl)
    - <span class="section-num">3.1</span> [Network Security SSL](#network-security-ssl)
        - <span class="section-num">3.1.1</span> [Exposing the Public IPs of Tor Services | Netsparker](#exposing-the-public-ips-of-tor-services-netsparker)
        - <span class="section-num">3.1.2</span> [Deciphering Malware’s use of TLS (without Decryption)](#deciphering-malware-s-use-of-tls--without-decryption)
- <span class="section-num">4</span> [Network Tor](#network-tor)
    - <span class="section-num">4.1</span> [Tor research](#tor-research)
        - <span class="section-num">4.1.1</span> [pylls (pulls)](#pylls--pulls)
- <span class="section-num">5</span> [Network SMTP](#network-smtp)
- <span class="section-num">6</span> [Network Security SMTP](#network-security-smtp)
- <span class="section-num">7</span> [Remote Desktop Services](#remote-desktop-services)
    - <span class="section-num">7.1</span> [Brute force attacks increase due to more open RDP ports - Malwarebytes Labs | Malwarebytes Labs](#brute-force-attacks-increase-due-to-more-open-rdp-ports-malwarebytes-labs-malwarebytes-labs)

</div>
<!--endtoc-->



## <span class="section-num">1</span> Network DNS {#network-dns}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:56] </span></span> <- [Golang DNS](my-golang.md)
-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-20 Fri 21:15] </span></span> <- [Network Protocol](#network-protocol)
-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-08 Sun 18:05] </span></span> -> [Rust DNS](my-rust.md)


### <span class="section-num">1.1</span> [ogham/dog: Command-line DNS client](https://github.com/ogham/dog) {#ogham-dog-command-line-dns-client}


### <span class="section-num">1.2</span> [GitHub - pymumu/smartdns: A local DNS server to obtain the fastest website IP for the best Internet experience， 一个本地DNS服务器，获取最快的网站IP，获得最佳上网体验。](https://github.com/pymumu/smartdns) {#github-pymumu-smartdns-a-local-dns-server-to-obtain-the-fastest-website-ip-for-the-best-internet-experience-一个本地dns服务器-获取最快的网站ip-获得最佳上网体验}


### <span class="section-num">1.3</span> DNS Script {#dns-script}


#### <span class="section-num">1.3.1</span> [Quickpost: nslookup Types | Didier Stevens](https://blog.didierstevens.com/2019/07/03/quickpost-nslookup-types/) {#quickpost-nslookup-types-didier-stevens}


### <span class="section-num">1.4</span> Network [Security Project or Idea]({{< relref "security" >}}) DNS {#network-security-project-or-idea--security-dot-md--dns}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-20 Fri 21:22] </span></span> -> [ZeeK Script DNS<code>[0/0]</code>​](awesome-zeek.md)


#### <span class="section-num">1.4.1</span> detecting-dns-tunneling {#detecting-dns-tunneling}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-20 Fri 21:31] </span></span> <- [hhzzk/dns-tunnels](awesome-zeek.md)
-   [Heyoka - DNS Tunneling 2.0](http://heyoka.sourceforge.net/heyoka-shakacon2009.pdf)
    -   [Detecting DNS Tunneling](https://www.sans.org/reading-room/whitepapers/dns/detecting-dns-tunneling-34152)


## <span class="section-num">2</span> Network Protocol {#network-protocol}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-20 Fri 21:15] </span></span> -> [Network DNS](#network-dns)


## <span class="section-num">3</span> Network SSL {#network-ssl}


### <span class="section-num">3.1</span> Network Security SSL {#network-security-ssl}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 01:58] </span></span> <- [Zeek Script SSL](awesome-zeek.md)
-   [Security Project or Idea]({{< relref "security" >}})

:ID:       2c444f27-0893-449f-96ea-21f8df6d99e5


#### <span class="section-num">3.1.1</span> [Exposing the Public IPs of Tor Services | Netsparker](https://www.netsparker.com/blog/web-security/exposing-public-ips-tor-services-through-ssl-certificates/) {#exposing-the-public-ips-of-tor-services-netsparker}


#### <span class="section-num">3.1.2</span> Deciphering Malware’s use of TLS (without Decryption) {#deciphering-malware-s-use-of-tls--without-decryption}

<!--list-separator-->

1.  [1607.01639.pdf](https://arxiv.org/pdf/1607.01639.pdf)


## <span class="section-num">4</span> Network Tor {#network-tor}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:04] </span></span> <- [Detecting Tor traffic with Bro network traffic analyzer - Stephen Reese](awesome-zeek.md)


### <span class="section-num">4.1</span> Tor research {#tor-research}


#### <span class="section-num">4.1.1</span> [pylls (pulls)](https://github.com/pylls?tab=overview&from=2019-12-01&to=2019-12-31) {#pylls--pulls}


## <span class="section-num">5</span> Network SMTP {#network-smtp}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:26] </span></span> <- [initconf/smtp-url-analysis: Extracting and analyzing URLs from Emails for phishing events](awesome-zeek.md)


## <span class="section-num">6</span> Network Security SMTP {#network-security-smtp}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:21] </span></span> <- [initconf/phish-analysis: Suite of smtp related policies includes extracting and logging URLs from emails and various smtp anomaly detection heuristics to help flag phishing emails](awesome-zeek.md)
-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:20] </span></span> <- [Network attack detection](security.md)


## <span class="section-num">7</span> Remote Desktop Services {#remote-desktop-services}

-   <span class="timestamp-wrapper"><span class="timestamp">[2020-11-22 Sun 02:37] </span></span> <- [Zeek RDP detection](awesome-zeek.md)

Remote Desktop Services (RDS), known as Terminal Services in Windows Server 2008 and earlier, is one of the components of Microsoft Windows that allow a user to take control of a remote computer or virtual machine over a network connection. RDS is Microsoft's implementation of thin client architecture, where Windows software, and the entire desktop of the computer running RDS, are made accessible to any remote client machine that supports Remote Desktop Protocol (RDP). User interfaces are displayed from the server onto the client system and input from the client system is transmitted to the server - where software execution takes place.


### <span class="section-num">7.1</span> [Brute force attacks increase due to more open RDP ports - Malwarebytes Labs | Malwarebytes Labs](https://blog.malwarebytes.com/exploits-and-vulnerabilities/2020/10/brute-force-attacks-increasing/) {#brute-force-attacks-increase-due-to-more-open-rdp-ports-malwarebytes-labs-malwarebytes-labs}
