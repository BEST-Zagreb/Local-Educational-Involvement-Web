# Local Educational Involvement (LEI), 2024 conference site

Static archive of the LEI blog that ran at `localeducationalinvolvement.wordpress.com`. LEI was a one day student conference held by BEST Zagreb with the Student Council of the University of Zagreb on 12 April 2024 (Kino Forum, SD Stjepan Radić), with talks and panels on STEM higher education and engineering careers. This repository used to hold a one page redirect to that blog; the blog itself is now archived here as plain HTML, and it is the only copy, since the Wayback Machine never captured the site.

Live at <https://lei.best.hr/>.

## What is in it

The landing page (the whole conference in Croatian: topics, date, venue, partners, sign up link), the announcement post from 21 March 2024, the "Informacije o nama" page, the author and category listings, and six posts from March 2024 that are WordPress's Twenty Twenty-Four sample content, left in because they were published on the public blog. Eleven pages, 65 files, 3.9 MB. The landing page's "Novosti" section is empty on the original as well; the posts were reachable only by direct address there too.

## Where it comes from

There was no login to the WordPress.com account, so everything was taken from the public site. The page list was built from the sitemap, the RSS feed and every internal link until nothing new appeared. Each page was fetched as served, images came from the blog host in every size the pages ask for, and the theme fonts came from `s0.wp.com` and `fonts.wp.com`; they sit under folders named after those hosts. Every reference was rewritten to a relative path, so the site works from any sub-path with no server, no database and nothing to keep patched.

Checked afterwards: all 56 URLs a browser would request answered 200 from a local server, every page rendered in Chromium with zero broken images and zero requests to any host other than the server, and the visible text and images of all eleven pages are identical to the live blog once the WordPress.com chrome below is removed from both.

## What was removed, and why

A free WordPress.com blog wraps every page in things that only work on WordPress.com and mostly report back to it: the "Design a site like this" marketing bar, the follow/subscribe and log in bar, the cookie consent stub, the stats and performance beacons, Jetpack likes, sharing buttons, the comment form (it posted to wordpress.com), the "Blog pokreće WordPress.com" footer credit, the abuse report link, and the feed, RSD, OpenSearch and oEmbed links in the head. All of it is gone, along with every script on the pages (there were none the content needs; the theme renders with CSS alone). The one link in the sample page that pointed into the WordPress.com dashboard was unlinked, its text kept. Facebook, Instagram, LinkedIn and the Google Form sign up link are untouched.

Personal contact details were checked for as on the other BEST archives; the blog contains none, so nothing had to be replaced.

## How to regenerate

`tools/lei-freeze.sh` in the migration notes alongside the other archives does it end to end while the blog is still up: `lei-pages.py` lists the pages, `lei-strip.py` removes the chrome, `lei-assets.py` fetches and relinks the assets, then the shared verify, compare and crawl tools run. Two runs produce the same folder byte for byte.

The Twenty Twenty-Four theme fonts (Inter, Cardo) are under the SIL Open Font License; the content and images belong to BEST Zagreb.

## Hosting

Live at <https://lei.best.hr/>, served by Cloudflare Workers as static files straight from this repository.
This repository is archived and read-only: the site it holds is finished. If something must change, unarchive it, push to `main`, and Workers Builds redeploys within a minute or two.

## Wayback Machine

The blog ran at <https://localeducationalinvolvement.wordpress.com/> and the redirect page at <https://lei.best.hr/>. The calendars are <https://web.archive.org/web/*/https://localeducationalinvolvement.wordpress.com/*> and <https://web.archive.org/web/*/https://lei.best.hr/*>.
Checked on 2026-09-11: the archive held nothing at all for the blog before a capture was requested that day. For lei.best.hr it holds 6 URLs, one of them an HTML page, captured between 2024-03-29 and 2025-01-25.
This repository is the complete copy of the blog; the archive is a partial, independent second copy at best.
