---
layout: post
title: W3 Total Cache Kullanım Rehberi
date: '2020-12-21'
author: Hakan Yerlikaya
permalink: /w3-total-cache/
subtitle: Wordpresss için W3 Total Cache eklentisi ile beraber Cloudflare kullanım rehberi.
---

Wordpress için W3 Total Cache eklentisi ile beraber ücretsiz olarak dağıtılan Cloudflare CND ağını etkinleştirerek web sayfaların yavaş açılma probleminin birazcıkta olsa önüne geçeceğiz.

Site hızı Google için bir sıralama sinyalidir.

Aşağıda paylaştığım mobil ve masaüstü cihazlar için hız testi ölçmeye yarayan araçları kullanarak çıkan sonuçları bir köşeye not almayı unutmayınız!

* <a href="https://web.dev/measure/" target="_blank" rel="noreferrer noopener">Measure Web.dev</a>
* <a href="https://developers.google.com/speed/pagespeed/insights/" target="_blank" rel="noreferrer noopener">Google PageSpeed Insights</a>
* <a href="https://www.thinkwithgoogle.com/intl/tr-tr/feature/testmysite/" target="_blank" rel="noreferrer noopener">Test My Site</a>

<img alt="Measure Web.dev" title="Measure Web.dev" src="/img/Measure-Webdev.png">
<img alt="Google PageSpeed Insights" title="Google PageSpeed Insights" src="/img/Google-PageSpeed-Insights.png">
<img alt="Test My Site" title="Test My Site" src="/img/Test-My-Site.png">

<h2> W3 Total Cache </h2>


W3 Total Cache eklentisinin kurulumu için aşağıdaki adımları takip ederek kurulumunu tamamlayınız.

* Eklentiler
* Yeni Ekle
* W3 Total Cache
* Şimdi Kur
* Etkinleştir

<img alt="W3 Total Cache Şimdi Kur" title="W3 Total Cache Şimdi Kur" src="/img/Wordpress-W3-Total-Cache-Simdi-Kur.png">

<img alt="W3 Total Cache Etkinleştir" title="W3 Total Cache Etkinleştir" src="/img/Wordpress-W3-Total-Cache-Etkinlestir.png">

<h3> General Settings </h3>

* Page Cache: Enable
  * Page Cache Method: Disk: Enhanced
* Minify: Disable
  * Minify Mode: Auto
  * Minify Cache Method: Disk
* Opcode Cache: Not Available
* Database Cache: Disable
  * Database Cache Method: Disk
* Object Cache: Enable
  * Object Cache Method: Disk
 * Browser Cache: Enable 
* Lazy Load Images: Enable
  * Disable Emoji: Enable
  * Disable wp-embed script: Enable
  * Disable jquery-migrate on the front-end: Enable
* Fragment Cache Method: Disk

<img alt="W3 Total Cache General Settings" title="W3 Total Cache General Settings" src="/img/W3-Total-Cache-General-Settings.png">

<h3> Page Cache </h3>

* Cache front page: Enable
* Cache feeds: site, categories, tags, comments: Enable
* Cache SSL (HTTPS) requests: Enable
* Cache URIs with query string variables: Disable
* Cache 404 (not found) pages: Disable
* Don't cache pages for logged in users: Enable
* Don't cache pages for following user roles: Enable
  * Administrator 
  * Editor
  * Author
  * Contributor
  * Subscriber
Bu sekmede sitemap URL bölümüne web sayfanızın site haritası yolunu ekleyiniz.

* Automatically prime the page cache: Enable
  * Update interval: 100 seconds
  * Pages per interval: 10
  * Sitemap URL:
* Preload the post cache upon publish events: Enable

<img alt="W3 Total Cache Page Cache" title="W3 Total Cache Page Cache" src="/img/W3-Total-Cache-Page-Cache.png">

<h3> Browser Cache </h3>

* Set Last-Modified header: Enable
* Set expires header: Enable
* Set cache control header: Enable
* Set entity tag (ETag): Enable
* Set W3 Total Cache header: Enable
* Enable HTTP (gzip) compression: Enable
* Enable HTTP (brotli) compression: Disable
* Prevent caching of objects after settings change: Disable
* Remove query strings from static resources: Enable
* Don't set cookies for static files: Enable
* Do not process 404 errors for static objects with WordPress: Disable
* Rewrite URL structure of objects: Disable

* Set Last-Modified header: Enable
* Set expires header: Enable
* Expires header lifetime: 31536000 seconds
* Set cache control header: Enable
* Set entity tag (eTag): Enable
* Set W3 Total Cache header: Enable
* Enable HTTP (gzip) compression: Enable
* Enable HTTP (brotli) compression: Disable
* Prevent caching of objects after settings change: Disable
* Remove query strings from static resources: Enable
* Disable cookies for static files: Enable

<img alt="W3 Total Cache Browser Cache" title="W3 Total Cache Browser Cache" src="/img/W3-Total-Cache-Browser-Cache.png">
