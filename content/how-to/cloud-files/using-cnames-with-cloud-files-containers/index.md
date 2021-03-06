---
permalink: using-cnames-with-cloud-files-containers/
audit_date:
title: Using CNAMEs with Cloud Files containers
type: article
created_date: '2011-04-27'
created_by: Rackspace Support
last_modified_date: '2018-10-23'
last_modified_by: Kate Dougherty
product: Cloud Files
product_url: cloud-files
---

A CNAME record is way to link your Cloud Files container to a branded
URL that you display instead of a CDN URL. For example, you might want
create a CNAME record that links your CDN URL (for example,
`https://c186397.r00.cf1.rackcdn.com`) to a shorter or branded URL (for
example, `https://images.mycompany.com`).

### Find your CDN URL

Before you can create the CNAME record, you need to know the CDN URL of
the container. You can find this information in the Cloud Files section of the
[Cloud Control Panel](https://login.rackspace.com/) by clicking the
gear icon next to the container name and selecting **View All Links**. A
popup dialog box with the CDN links to the container displays, as shown in the following image:

{{<image src="1080-2_2.png" alt="" title="">}}

Alternatively, you can request your container information by using the [Cloud
Files API](https://docs.rackspace.com/docs/cloud-files/v1/).

### Set up CNAME records

You set up your CNAME record by managing your DNS. Within your DNS
settings, request a new record. Ensure that your CNAME record points to
your container's CDN URL and not your object's CDN URL.

If you're using [Rackspace Cloud DNS](https://www.rackspace.com/cloud/dns),
creating a CNAME record that uses the example values introduced at the
beginning of this article look like the following image:

{{<image src="cnameadd.png" alt="" title="">}}

If you want to edit or delete your CNAME record, you can also do that by
managing your DNS in your existing tool.

**Notes:**

-   You are not charged extra for using CNAMEs.
-   At this time, CNAMEs do not work with SSL (or HTTPS) delivery.
