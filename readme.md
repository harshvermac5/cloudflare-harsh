# Abbreviations

- **CnC**: Command-and-Control Center
- **ARC**: Argonaut RISC Core
- **SSDP**: Simple Service Discovery Protocol
- **UPnP**: Universal Plug and Play
- **HOIC**: High Orbit Ion Cannon
- **IPRF**: IP Reputation Filtering
- **LOIC**: Low Orbit Ion Cannon
- **AFS**: Andrew File System
- **XMPP**: Extensible Messaging and Presence Protocol
- **SIP**: Session Initiation Protocol
- **ENUM**: Enumerated Type
- **DNSBL**: Domain Name System-based Blackhole List
- **MTA**: Message Transfer Agent
- **IETF**: Internet Engineering Task Force
- **IMAP**: Internet Message Access Protocol
- **ARPA**: Advanced Research Projects Agency
- **ZSK**: Zone Signing Keys
- **KSK**: Key Signing Key
- **RUA**: Reporting URI for Aggregate Reports
- **RFC**: Request for Comments
- **CPE**: Customer Premise Equipment
- **SOA**: Start of Authority
- **ISC**: Internet Systems Consortium
- **IXPs**: Internet Exchange Points
- **ESI**: Edge Side Includes
- **PNI**: Private Network Interconnect
- **GSLB**: Global Server Load Balancing
- **APO**: Automatic Platform Optimization

---

## DDoS Attack Categories

DDoS attacks can be divided into three categories:

- **Application Layer Attacks**
- **Protocol Attacks** (State-Exhaustion Attacks)
- **Volumetric Attacks**

---

## Solutions to DDoS

Some common solutions to mitigate DDoS attacks:

- **Blackhole Routing**
- **Rate Limiting**
- **Web Application Firewall**
- **Anycast**
- **Disable IP Broadcasting**
- **Disable ICMP**
- **Use of CAPTCHA**
- **JavaScript Computational Challenges**

---

## Botnet Models

There are three common botnet models:

- **Client-Server**
- **Tiered CnC**
- **Peer-to-Peer**

---

## Common DDoS Attacks

Types of common DDoS attacks:

- **L7 Application**
- **Cryptocurrency**
- **DNS Amplification**
- **L3**
- **Low and Slow Attack**
- **Memcached**
- **NTP Amplification**
- **Ransom DDoS**
- **SSDP Amplification**
- **Ping of Death**
- **Ping Flood**
- **Smurf**: Amplification attack but with Ping

---

## Cryptocurrency

### Blockchain

#### Mining

**Fast Flux**: A technique where attackers use rapidly changing IP addresses for malicious websites.

---

## Networking

**Handshake**: In networking, this refers to the process where both parties agree to establish a communication session.

---

## DNS Overview

- The **DNS Recursor** is a server that receives queries from clients, such as web browsers, to resolve domain names.
- The **Root Server** is the first step in resolving human-readable hostnames to IP addresses. For example, in `example.com`, the **TLD (Top-Level Domain) server** is `com`.
- If the **Authoritative Name Server** has the requested record, it will return the IP address for the hostname to the DNS Recursor.

### Query Resolution Behavior

- **Recursive Query**: The DNS resolver takes full responsibility for resolving the query and provides the final answer.
- **Non-Recursive Query**: The DNS resolver returns referrals for resolving the query but doesn't provide the final answer.

### Query Resolution Process

- **Iterative Resolution**: The client or DNS resolver queries the appropriate servers at each level of the DNS hierarchy until the final answer is obtained.
- **Recursive Resolution**: The resolver sends queries to other DNS servers, starting at the root and working down through TLD and authoritative servers until the final answer is found.

---

## DNS Records

- **A**: Maps a domain to an IPv4 address (e.g., 192.0.2.1).
- **AAAA**: Maps a domain to an IPv6 address (e.g., 2001:0db8::1).
- **CNAME**: The canonical name, forwards one domain or subdomain to another. It does not provide an IP address, acting as an alias.
- **MX**: Mail Exchange record, directs email traffic to the appropriate mail server for a domain.
- **TXT**: Stores text data in a DNS record, commonly used for verification or security purposes.
- **NS**: Specifies the authoritative name servers for a domain.
- **SOA**: Start of Authority record, stores administrative information about a domain.
- **SRV**: Service record, specifies a service and its corresponding port (used by protocols like SIP or XMPP).
- **PTR**: Pointer record, used for reverse DNS lookups, mapping IP addresses to domain names.

Additional DNS records:

- **DNSKEY**: Contains a public key for DNSSEC verification.
- **DS**: Delegation Signer record used for DNSSEC to secure delegated zones.
- **SPF**: Sender Policy Framework, specifies authorized mail servers for a domain.
- **DKIM**: DomainKeys Identified Mail, stores a public key to verify email signatures.
- **DMARC**: Defines email authentication policies using SPF and DKIM, facilitating email validation reporting.
- **AFSDB**: AFS Database record, used to locate other AFS cells.
- **APL**: Address Prefix List, experimental record specifying address ranges.
- **CAA**: Certification Authority Authorization, specifies authorized Certificate Authorities (CAs).
- **CDNSKEY**: A child copy of the DNSKEY record for DNSSEC validation.
- **CERT**: Stores public key certificates for SSL/TLS.
- **DCHID**: DHCP Identifier, stores information for DHCP.
- **DNAME**: Delegation Name, redirects all subdomains to a new domain (similar to CNAME).
- **HIP**: Host Identity Protocol, separates a host's identity from its IP address.
- **IPSECKEY**: Provides public keys for IPsec authentication.
- **LOC**: Stores geographical information (longitude, latitude).
- **NAPTR**: Name Authority Pointer, dynamically creates URIs based on regular expressions.
- **NSEC**: Next Secure record, used to prove the non-existence of DNS resource records (DNSSEC).
- **RRSIG**: Resource Record Signature, used for DNSSEC authentication of DNS records.
- **RP**: Responsible Person, stores the email address of the person responsible for the domain.
- **SSHFP**: SSH Fingerprint, stores fingerprints of SSH public keys.

### DNS Resolution in Email

The **Message Transfer Agent (MTA)** software is responsible for querying MX records to route emails. The MTA queries DNS to identify mail servers and then establishes an SMTP connection with them.

### SRV Record Behavior

In SRV records, servers with a lower **priority** receive more traffic. The **weight** value breaks ties if two servers have the same priority, with higher weight receiving more traffic.

---

## DNS Attacks

Types of DNS attacks include:

- **DNS Spoofing / Cache Poisoning**
- **DNS Tunneling**
- **DNS Hijacking**
- **NXDomain Attack**
- **Phantom Domain Attack**
- **Random Subdomain Attack**
- **Domain Lock-up Attack**
- **Botnet-Based CPE Attack**

**Cybersquatting** refers to the act of registering domain names that others may want to use, often violating trademarks, with the intent to extort money.

**Domain Parking** is the practice of registering a domain without actively using it, distinct from cybersquatting.

---

## Email Authentication

Email servers require both **SPF** (Sender Policy Framework) and **rDNS** (reverse DNS) to verify the legitimacy of the sending server. SPF confirms the server’s authorization, while rDNS checks that the sending server’s IP address matches its domain name.

---

## Recursion vs. Iteration

- **Recursion**: A process where a program repeatedly calls itself until a base condition is met.
- **Iteration**: A process where a set of instructions is repeated until a condition is met.

---

# CDN

### TLS False Start

TLS False Start improves data transfer timing by allowing encryption to begin earlier during the handshake process.

### ETag

An **ETag** is a unique token assigned to a resource version. When a resource changes, its ETag changes accordingly.

---

## Cache Control Directives

Common cache control directives include:

- `cache-control: private`
- `cache-control: public`
- `cache-control: no-store`
- `cache-control: no-cache`
- `cache-control: max-age`
- `cache-control: s-maxage`
