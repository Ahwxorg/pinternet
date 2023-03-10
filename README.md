<h2 align="center">Pinternet</h2>

> The main concept is that you don't want the random popups forcing you to log in, and you don't want a bunch of JS.


<h2 align="center">Showcase:</h2>
<p align="center">
  <img src="https://raw.githubusercontent.com/Ahwxorg/pinternet/main/misc/pinternet-1.png" width="350">
  <img src="https://raw.githubusercontent.com/Ahwxorg/pinternet/main/misc/pinternet-2.png" width="350">
</p>


<h2 align="center">Features:</h2>

* API-less Pinterest image searching.
* Pinterest doesn't see the IP of the end user, only the instance IP;
* Image proxy (thanks to [LibreX](https://github.com/hnhx/LibreX)'s code).


<h2 align="center">Instances:</h2>

> Make a PR to get added. CloudFlare is not allowed.

| Clearnet | TOR | Country |
|-|-|-|
| [pinternet.ahwx.org](https://pinternet.ahwx.org/) | no | 🇳🇱 NL (Official Instance) |
<br>


<h2 align="center">Install</h2>

Just clone it somewhere, make a reverse proxy rule and you're set. Example:

```sh
doas apt install php php-curl nginx nginx-common git
git clone https://git.ahwx.org/pinternet /var/www/html/pinternet
cd /var/www/html/pinternet
```

Example NGINX configuration:

```sh
server {
        listen 80;
        server_name pinternet.ahwx.org;

        root /var/www/html/pinternet;
        index index.php;

        location ~ \.php$ {
          include snippets/fastcgi-php.conf;
          fastcgi_pass unix:/run/php/php-fpm.sock;
        }
}
```



<h3 align="center">Credits:</h3>

* [LibreX](https://github.com/hnhx/librex) | [https://femboy.hu](https://femboy.hu) - image proxy & quite a bit of other code.


