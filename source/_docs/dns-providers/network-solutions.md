---
title: Network Solutions Domain Configuration
provider: Network Solutions
dnsprovider: true
description: Learn how to point your Network Solutions domain to a Pantheon site.
tags: [providers]
permalink: docs/:basename/
editpath: dns-providers/network-solutions.md/
---
## Before You Begin
Be sure that you have a:


- Registered domain name using Network Solutions to host DNS
- [Paid Pantheon plan](/docs/guides/launch/plans/)
- [Domain connected](/docs/guides/launch/domains/) to the target Pantheon environment (typically Live)

## Locate Pantheon's DNS Values
Identify DNS values to point your domain to Pantheon:

1. Navigate to the Site Dashboard and select the target environment (typically <span class="glyphicons glyphicons-cardio"></span> Live) then click **<span class="glyphicons glyphicons-home"></span> Domains & HTTPS**.
2. Click the **DNS Recommendations** button next to your domain.

Keep this page open and login to your <a href="https://godaddy.com/" target="blank">Network Solutions account <span class="glyphicons glyphicons-new-window-alt"></span></a> in a new tab before you continue.

## Configure DNS Records on Network Solutions
### A Record
1. Navigate to **Account Manager** > **My Domain Names**
2. Select the domain you want to point to Pantheon, then click **Manage**.
3. Click **Change Where Domain Points**, then select **Advanced DNS**.
4. In the IP Address (A records) section, click **Edit A Records**.
4. Enter **@** in the **Host** field and enter the A record value provided by Pantheon in the **Value** field.
5. Select desired Time to Live (TTL).

    {% include("ttl.twig") %}

6. Click **Save Changes**.

### AAAA Records
1. Click the **Add New Record** button and select **AAAA** from the type dropdown menu.
2. Enter **@** in the **Host** field and enter the first AAAA record value provided by Pantheon in the **Value** field.
3. Select desired Time to Live (TTL).
4. Click **Save**.
5. Repeat steps 1-4 for the second AAAA record value provided by Pantheon. There are two AAAA records for improved uptime and reliability.

### CNAME Record
The CNAME record is required if you wish to include `www` within your site's primary domain name.

1. In the Host Aliases (CNAME Records) section, click **Edit CNAME Records**.
2. Enter **www** in the **Host** field and enter the CNAME record value provided by Pantheon (e.g. `live-example.pantheonsite.io`) in the **Aliases** field.
3. Select desired Time to Live (TTL).
4. Click **Continue**, then **Save Changes**.


## Network Solutions Docs

<a href="http://www.networksolutions.com/support/how-to-manage-advanced-dns-records/" target="blank">Managing Advanced DNS Records <span class="glyphicons glyphicons-new-window-alt"></span></a>

## Next Steps

* [Launch Essentials: Domains & HTTPS](/docs/guides/launch/domains/)
* [Launch Essentials: Redirect to a Primary Domain](/docs/guides/launch/redirects/)
