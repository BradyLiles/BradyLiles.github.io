---
layout: post
title:  "Open Discussion on Jekyll!"
date:   2015-06-08 12:00:00
tags: test comments, discussion, disqus
categories: testing
comments: true
---
We can now have a great conversation on a static site using <a href="https://disqus.com/">Disqus!</a>
This is pretty interesting knowing how easy and little code it takes to allow conversation on a site using Jekyll or just plain html. 
Simply register for an account on Disqus, select the option to get the Universal Embed Code.
Copy and paste the code on any page or put it in one of the layout pages.

The code is very minimal:


``` html
{% if page.comments %}
<div id="disqus_thread"></div>
<script type="text/javascript">
    var disqus_shortname = 'myForumnName'; // required: replace example with your forum shortname
    var disqus_identifier = "{{ page.url }}";

    (function() {
        var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
        dsq.src = '//' + disqus_shortname + '.disqus.com/embed.js';
        (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="http://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
<a href="http://disqus.com" class="dsq-brlink">comments powered by <span class="logo-disqus">Disqus</span></a>
{% endif %}
```