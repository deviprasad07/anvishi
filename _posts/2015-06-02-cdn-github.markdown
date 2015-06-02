---
layout: post
title:  "Using AWS CDN to host files"
date:   2015-06-02 15:10:00
categories: misc
---
I am thoroughly enjoying maintaining my website on Github. Jekyl is great, Github is great as a host too but only for small files. If you need to upload large images or binaries, you will, sooner or later, run into their hard limit of 100MB. And it makes sense too. Git is meant for version control, which means every version is stored. Versioning large files would make it really slow. Thus, I decided to move all my static files (except css/js) to Cloudfront (AWS CDN) and S3 (AWS Object storage service).

To achieve the goal, I first created a S3 bucket with a directory in it that would serve all public files. A S3 bucket by default is not visible to the public. However, to use it with Cloudfront it should be (obvious right). To make my cloudfront bucket public I added the following policy:

<script src="https://gist.github.com/adeydas/dbf5f705061786a3833e.js"></script>

*Replace BUCKETNAME with the name of your bucket*

Next I added View permissions for "Everyone". The panel for that is available under Properties > Permissions.

![S3 properties](http://cdn.abhis.ws/cdn/blog-images/cdn2.png)

Next on the list was setting up CloudFront. This was the easy part. The S3 bucket containing the files should be selected for "Origin Domain Name". If you want to use a custom domain instead of *gibberish.cloudfront.net* (mine is cdn.abhis.ws), you need to feel that under "Alternate Domain Names" and point a CNAME record to your cloud front subdomain. I left the rest of the options alone.

It took a few minutes to deploy and every upload takes a couple of seconds to propagate but I got a fantastic and cheap CDN working now.