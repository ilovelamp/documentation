---
title: eNom Domain Configuration
provider: eNom
dnsprovider: true
description: Learn how to point your eNom domain to a Pantheon site.
tags: [providers]
permalink: docs/:basename/
editpath: dns-providers/enom.md/
---
## Before You Begin
Be sure that you have a:


- Registered domain name using eNom to host DNS
- [Paid Pantheon plan](/docs/guides/launch/plans/)
- [Domain connected](/docs/guides/launch/domains/) to the target Pantheon environment (typically Live)

## Configure DNS Records on eNom
### A Record
1. Navigate to **Domains** > **My Domains**.
2. Click on the domain you want to point to Pantheon.
3. Select **Host Records**.
4. Click **New Row**.
5. Enter **@** in the **Host Name** field, select **A** for the **Record Type** then enter the A record value provided by Pantheon in the **Address** field.

### AAAA Records
1. Click **New Row**.
2. Enter **@** in the **Host Name** field, select **AAAA** for the **Record Type** then enter the first AAAA record value provided by Pantheon in the **Address** field.
3. Repeat steps 1-2 for the second AAAA record value provided by Pantheon. There are two AAAA records for improved uptime and reliability.

### CNAME Record
The CNAME record is required if you wish to include `www` within your site's primary domain name.

1. Click **New Row**.
2. Enter **www** in the **Host Name** field, select **CNAME** for the **Record Type** then enter the CNAME record value provided by Pantheon (e.g. `live-example.pantheonsite.io`) in the **Address** field.
4. Click **Save**.

## eNom Docs

<a href="https://www.enom.com/kb/kb/kb_0002_change-host-records.htm" target="blank">Change Host Records - Forward, Redirect or Point Your Domain/Sub-Domain
 <span class="glyphicons glyphicons-new-window-alt"></span></a>

## Next Steps

* [Launch Essentials: Domains & HTTPS](/docs/guides/launch/domains/)
* [Launch Essentials: Redirect to a Primary Domain](/docs/guides/launch/redirects/)
