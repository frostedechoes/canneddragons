---
title: "Mozilla Has All The Cookies"
date: 2021-02-24 23:51:00 +0000
Link: /2021/02/24/mozilla-has-all.html
Tags: tech
---

# Mozilla Has All The Cookies

<p>On the <a href="https://blog.mozilla.org/security/2021/02/23/total-cookie-protection/">Mozilla Security blog</a>, the Firefox team details their new implementation of cross-site browsing protection by keeping cookies from each site you visit in their own, separate containers. Firefox has had the ability to use different containers with separate cookies explicitly for some time with their “Containers” feature (I love to use this for testing with different identities on the same site). </p>


<p>This new implementation will make cross-site tracking much more difficult. You may no longer find yourself wondering how they knew you were looking for a new couch when you see the ads on your favorite news site. This should turn down the creepiness factor of using the internet. </p>

<img src="https://frostedechoes-test.micro.blog/uploads/2021/e35dc06041.png" alt="Total Cookie Protection illustration by Meghan Newell" />

<p>I was concerned about the legitimate uses of some cross-site cookies, but it seems they have have that covered.</p>

<blockquote>
<p>In addition, Total Cookie Protection makes a limited exception for cross-site cookies when they are needed for non-tracking purposes, such as those used by popular third-party login providers. Only when Total Cookie Protection detects that you intend to use a provider, will it give that provider permission to use a cross-site cookie specifically for the site you’re currently visiting. Such momentary exceptions allow for strong privacy protection without affecting your browsing experience.</p>
</blockquote>

<p>I hope beta testers are hitting this use case pretty hard, because I could see issues occurring there more than any place else. If that works, though, this could be the strongest step yet by a mainstream browser in protecting privacy on the web. </p>