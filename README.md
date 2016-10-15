# chrome-extension-kcjs

In February 2013, Comcast implemented a Copyright Alert System, "a six-step approach designed to notify and educate customers about allegations of copyright infringement occurring over their Internet service".

For details on the six-stages of the alert system...http://corporate.comcast.com/comcast-voices/comcast-launches-copyright-alert-system

Addititional background from Ars Technica...http://arstechnica.com/tech-policy/2013/02/heres-what-an-actual-six-strikes-copyright-alert-looks-like/

Comcast describes the alert system as an "in-browser alert", which shows up in your browser as a popup overlay on any page you're browsing. If you look at the source code of the page you're browsing, you can see that Comcast is simply intercepting the HTML file for the page you're browsing and then appending a DIV element to act as the alert overlay. 

Comcast Copyright Alert System - Alert #4
![Alt text](/images/comcast_cas_alert4.jpg?raw=true "CAS4")

This Chrome extension is a simple one-liner to remove the added alert overlay element via the following JS code...

<code>document.getElementById('comcast_content').remove();</code>


