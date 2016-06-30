---
layout: post
title:  "Installation de cloud9 IDE sur Raspberry pi"
date:   2016-06-28 15:00:00 +0000
categories: raspberry cloud9
---
J'utilise de plus en plus la plateforme de développement [cloud9](http://c9.io) qui permet de disposer d'un ensemble
d'environnement customisable. J'apprécie son IDE qui reconnait la plus part des langages usuels. De plus il permet
l'accès à plusieurs terminaux et fenêtres d'édition.

## Installation

Suivez ces quelques étapes pour installer c9sdk sur votre rapsberry pi

{% highlight Shell %}
~/ $ git clone git://github.com/c9/core.git c9sdk
~/ $ cd c9sdk
~/c9sdk $ scripts/install-sdk.sh
{% endhighlight %}
    
Vous en avez pour quelques heures...
    
## Démarrez CLOUD9

En mode local :

{% highlight Shell %}
~/c9sdk $ node server.js -p 8080 -a
        Starting standalone
        Connect server listening at http://127.0.0.1:8080
        CDN: version standalone initialized /home/pi/c9sdk/build
        Started 'home/pi/c9sdk/configs/standalone' with config 'standalone'!
        Cloud9 is up and running
{% endhighlight %}
    
Ou, pour une utilisation depuis un autre ordinateur :

{% highlight Shell %}
~/c9sdk $ node server.js --listen %IP% -p 8080 -a user:password
{% endhighlight %}
    
La configuration prend un certain temps...

![Cloud9_IDE](/images/Cloud9.png)
    
Vous pouvez maintenant développer sur votre raspberry pi depuis
tout appareil disposant d'un navigateur internet.


