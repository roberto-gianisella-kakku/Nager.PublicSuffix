Nager.PublicSuffix
==========
publicsuffix.org a list of known public domain suffixes (TLD). Some example .com, .co.uk, co.at. The current data loads from https://publicsuffix.org. This library does not nees a additional cache system is very fast on different domain names.

### nuget
The package is available on [nuget](https://www.nuget.org/packages/Nager.PublicSuffix)
```
PM> install-package Nager.PublicSuffix
```

### Donation possibilities
If this project help you reduce time to develop, you can give me a beer :beer:
- [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.me/nagerat/25)
- BTC: 3PjuVRcAaKPv9yLLmrVUY9mqGngPDm3nPc (Bitcoin)

### Exampels

#### Load data from publicsuffix.org
```cs
var domainParser = new DomainParser(new WebTldRuleProvider());

var domainName = domainParser.Get("sub.test.co.uk");
//domainName.Domain = "test";
//domainName.Hostname = "sub.test.co.uk";
//domainName.RegistrableDomain = "test.co.uk";
//domainName.SubDomain = "sub";
//domainName.TLD = "co.uk";
```

#### Load data from file
```cs
var domainParser = new DomainParser(new FileTldRuleProvider("effective_tld_names.dat"));

var domainName = domainParser.Get("sub.test.co.uk");
//domainName.Domain = "test";
//domainName.Hostname = "sub.test.co.uk";
//domainName.RegistrableDomain = "test.co.uk";
//domainName.SubDomain = "sub";
//domainName.TLD = "co.uk";
```
