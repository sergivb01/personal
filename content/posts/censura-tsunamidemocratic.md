+++
date = "2019-10-19"
title = "Tsunami Democràtic Censorship"
slug = "tsunami-censorship"
description = "How has the censorship against Tsunami Democràtic websites been applied and how to bypass it."
+++
# What is Tsunami Democràtic
-- TODO

## Domains
The organization several domains, such as `tsunamidemocratic.cat` and `democratictsunami.eu`, both of which were bought via *Tucows Domains Inc.* on the **13rd of July 2019** and use [Cloudflare](https://cloudflare.com) domain name servers and protect against attacks.

The organization's web was made up of two websites, one to distribute and publish the application used to organize the protests and another for the organization itself. Few days after the riots started a new version of the website was published and both sites were merged into a single one.

## Hosting
The application website (`app.tsunamidemocratic.cat`) was hosted in [GitHub Pages](https://pages.github.com) using the GitHub account of [s3rrallonga](https://github.com/s3rrallonga), a Catalan brigand likely to *Robin Hood* ([more info](https://www.sapiens.cat/temes/personatges/qui-era-serrallonga_17330_102.html)). The repository [s3rrallonga.github.io](https://github.com/s3rrallonga/s3rrallonga.github.io) has more than **32 forks** and **40 stars**, even tho the organization itself has not published the repository themselves. It also has few issues where people asked for an iOS version of the application and some other minor application issues.

The first version of main website (`tsunamidemocratic.cat`) hosting still not known, but the latest version is also being hosted using **GitHub Pages** via the GitHub organization of [tsunamidemocratic](https://github.com/tsunamidemocratic), which has no members. The [only repository that the organization has](https://github.com/tsunamidemocratic/tsunamidemocratic.github.io) is the one containing the website and, in contrast as the other repository, has **issues disabled** but is accepting **pull requests** (just a single one, which appears to be a silly joke).

Both repositories commits history may let us know that there are several people working on these websites as commit authors are different (s3rrallonga, **root** and **Jean**), though the only one linked to a GitHub account is **s3rrallonga**.

## How the takedown was effected
The Spanish Justice has stated that is investigating *Tsunami Democràtic* for terrorism and as a consequence has decided to take down their websites. For that, the [DNS Servers](https://www.cloudflare.com/learning/dns/what-is-a-dns-server) from the main Spanish Internet Service Providers have **altered the DNS responses** from the different domains that lead to the websites, including a bunch of [mirrors](https://en.wikipedia.org/wiki/Mirror_website) published in **Anonymous Catalonia**'s [Telegram channel](https://t.co/anoncatalonia).

<img src="/images/tsunami-mirrors.jpg" alt="" style="display: block; margin: 1rem auto;">

Tweet from [@Guardiacivil](https://twitter.com/guardiacivil) announcing the takedown of the websites.
{{< tweet 1185201502694137858 >}}

People whose ISP's DNS Servers participated in the takedown and had not changed the DNS servers on their devices were the only ones that were affected during the censorship. As the following image shows, using Cloudflare's [DNS Servers](https://1.1.1.1) you can access the different websites, while using [Movistar](https://www.movistar.es) (also known as Telefonica) DNS servers you can't access the website.

{{< figure src="/images/tsunami-takedown-notaffected.jpg" caption="Original website, content displayed to people not affected" link="http://tsunamidemocratic.github.io" target="blank" >}}

Funnily enough, the domain `tsdem.org`, after being censored, has been redirected to the [Human Rights Declaration](https://www.un.org/en/universal-declaration-human-rights) from the United Nations, via a Cloudflare Web Rules (as the follow image shows).

{{< figure src="/images/tsunami-redirect-humanrights.jpg" caption="Screenshot of the request to tsdem.org, using Chrome Devtools" >}}

## Censorship Website
As commented previously, affected users were redirected to `http://82.223.97.47`, which appears to be hosted in [Ionos](https://www.ionos.es), also known as *1and1*, is served via [Nginx](https://www.nginx.com) and managed by [Plesk](https://www.plesk.com) (as port `8443` is open in the server, which you can use to access Plesk panel).

{{< figure src="/images/tsunami-takedown.jpg" caption="Website you got redirected to if you were affected by the censorship" link="http://82.223.97.47" target="blank" >}}
