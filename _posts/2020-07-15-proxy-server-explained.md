---
layout: post
title: 
---
# Proxy Server Explained

![Proxy%20Server%20Explained%20c89763d474384634b5c7fecbbd8e71ed/proxy-illustration.png](Proxy%20Server%20Explained%20c89763d474384634b5c7fecbbd8e71ed/proxy-illustration.png)

A proxy server is just a computer configured in a special way. Using a proxy is just like asking another computer(the proxy) to get the web site you wanted for you. That's it. Simples.

## How you normally get a web page

1. You type a web address in to your browser
2. Your computer (after a DNS lookup) goes and connects directly to the web server that has the web site

## How you get a web page using a proxy

Let's assume you've already set your computer up to use a proxy.

1. You type a web address into your browser
2. Your computer sends the request to the proxy
3. The proxy (after a DNS lookup) connects to the web site you wanted
4. Once the proxy has the web page it hands it to your computer.

## Why use a proxy server?

### Control

Most work places want to block their employees from accessing certain websites. They do this by forcing all work computers to use a proxy. When you try to access something on you're not allowed to, the proxy will return an error page explaining access has been blocked.

### Security

Proxies can increase security by blocking access to known maliious sites thereby protecting users.

The proxy also acts as a shield. When all your internet traffic goes through a proxy your computer doesnt need to touch the internet. The only thing on the internet is your proxy server. If it gets hacked it's not such a big deal, your personal machine is protected. Proxies are usually build so they can't be hacked.

### Privacy

If you work at the NY Times or MIT, you may not want people to know the databases you’re searching or the people you are talking with on Skype. So running requests through a proxy server shields end user identity by shielding the identity (IP address) of your computer.

### Speed

This is more relevant when you have lots of users such as a work place and have a company proxy setup locally. By using a proxy, the proxy can cache (save) pages that it's already been asked to get. When another user wants the same web page the proxy can just serve that page quickly as it already has it saved locally rather than the users computer having to get the web page delviered to it over the web.

### Bypass censorship

Countries like China block access to certain web sites. A user could configure their computer to use a proxy that doesnt block anything. To the Chinese Government it would look like you are just connecting to another computer somwhere on the internet. Please note the proxy must not be one the Chinese Government know about else they could just block your access to the proxy.