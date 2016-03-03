YOURLS-GA-MP-Tracking
====================

Track YOURLS link clicks with Google Analytics Measurement protocol in Real Time

YOURLS.org is a best cumstom URL shortner script in PHP. YOURLS has many usefull plugins. I've build this plugin for track link clicks in real time with Google Analytics. Already few plugins available for this purpose. Unfortunately  they are not working. So I've build my own plugin. It is working perfectly. 

<h3>Start Up</h3>

* Create New Account Property in Google Analytics - Universal Analytic (Important)
* Get Tracking ID (Eg: UA-43862376-6)
* cd to user/plugins and `git clone https://github.com/Efreak/YOURLS-GA-MP-Tracking GA-MP-Tracking` and replace your GA Tracking code on line 64 (<b>$power_ga_mp_GAID</b>) in plugin.php
* Upload <b>GA-Measurement-Protocol</b> folder to /user/plugins/ path. (html/YOURLS INSTALL PATH/user/plugins/)
* Go to manage plugins in your YOURLS Admin interface and Activate it.

Now short &amp; share a link and watch clicks in Google Real Time reporting!

I've planned to use Google Event tracking for deep YOURLS click tracking in future (Eg: Track User IP, Click counts, Redirect time and more)

* I've used "pre_redirect" function for track every click.
* Please use Universal GA property. It is only support to Measurement protocol.

<h5>Note</h5>
Now Google Analytics shows  <b>Missing Tracking Code Page "yourShortUrl.com" for property "Custom Property" is missing valid tracking code</b> You can ignore this message. 

Keep in Touch with me on [@powerthazan](https://twitter.com/powerthazan)

* Browse more YOURS plugins [here](https://github.com/YOURLS/YOURLS/wiki/Plugin-List)

<h4>Version 1.1</h4>
Now, Real Time visitor location track-able.
There was no way to pass the end-user's IP or Geolocation (derived by GA from IP) to  the measurement protocol when I started to develop this plugin.


Now Google Add uip paramater for IP Override. It is helping to determine user location from GA End point. The source of the traffic arriving to the short url domain is now availble in Reports.
