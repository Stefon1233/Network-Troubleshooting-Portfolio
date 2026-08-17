# Scenario 12 - DNS Record Analysis

## Objective

Analyze multiple DNS record types to understand how domain names map to network services and how DNS information can be used during network troubleshooting.

## Tools Used

- Terminal
- dig
- macOS
- DNS

## Scenario

A user is able to access the internet but reports problems reaching specific online services. DNS records were examined to verify domain resolution, IPv4 and IPv6 addressing, 
mail routing, authoritative name servers, TXT records, and aliases.

## Tests Performed

### 1. A Record Lookup

Command:

`dig +short github.com A`

Result:

`140.82.113.4`

The A record successfully resolved `github.com` to an IPv4 address.

### 2. AAAA Record Lookup

Command:

`dig +short google.com AAAA`

Result:

`2607:f8b0:4009:802::200e`

The AAAA lookup returned an IPv6 address for `google.com`, confirming IPv6 DNS resolution.

### 3. MX Record Lookup

Command:

`dig +short github.com MX`

Result:

`0 github-com.mail.protection.outlook.com.`

The MX record identifies the mail server responsible for receiving email associated with the domain.

### 4. NS Record Lookup

Command:

`dig +short github.com NS`

Multiple authoritative name servers were returned, including AWS DNS servers and NS1 infrastructure.

Examples included:

- `ns-520.awsdns-01.net.`
- `ns-1283.awsdns-32.org.`
- `ns-1707.awsdns-21.co.uk.`
- `ns-421.awsdns-52.com.`
- `dns1.p08.nsone.net.`
- `dns2.p08.nsone.net.`
- `dns3.p08.nsone.net.`
- `dns4.p08.nsone.net.`

This confirmed that authoritative DNS infrastructure was available for the domain.

### 5. TXT Record Lookup

Command:

`dig +short github.com TXT`

Multiple TXT records were returned.

The records included domain-verification information and an SPF policy used to identify systems authorized to send email for the domain.

TXT records are commonly used for:

- Domain ownership verification
- Email authentication
- SPF policies
- Service configuration

### 6. CNAME Record Lookup

Command:

`dig +short www.github.com CNAME`

Result:

`github.com.`

This shows that `www.github.com` is configured as an alias pointing to the canonical `github.com` hostname.

## Troubleshooting Analysis

The DNS tests successfully returned A, AAAA, MX, NS, TXT, and CNAME records.

The A and AAAA lookups demonstrated successful IPv4 and IPv6 name resolution.

The MX lookup confirmed that mail-routing information could be retrieved.

The NS lookup identified the authoritative DNS infrastructure responsible for the domain.

TXT records demonstrated how DNS can also contain verification and email-security information.

The CNAME lookup demonstrated how one hostname can act as an alias for another hostname.

No DNS resolution failure was observed during testing.

## Resolution

DNS resolution was functioning normally for the tested domains. Multiple DNS record types were successfully retrieved and analyzed.

If a user were experiencing a DNS-related connectivity problem, these tests could help determine whether the issue involved:

- Missing DNS records
- Incorrect IP resolution
- Mail-routing configuration
- Authoritative DNS configuration
- Domain aliases
- DNS server availability

## Skills Demonstrated

- DNS troubleshooting
- `dig` command usage
- IPv4 DNS resolution
- IPv6 DNS resolution
- A record analysis
- AAAA record analysis
- MX record analysis
- NS record analysis
- TXT record analysis
- CNAME record analysis
- Network troubleshooting
- Command-line diagnostics

## Evidence

- `Screenshots/12-DNS-Record-Analysis/01-Address-and-Mail-Records.png`
- `Screenshots/12-DNS-Record-Analysis/02-NS-TXT-and-CNAME-Records.png`

## Conclusion

This scenario demonstrated how DNS records can be queried and analyzed during network troubleshooting. The tests confirmed successful name resolution and provided information 
about addressing, mail routing, authoritative DNS servers, TXT records, and hostname aliases.
