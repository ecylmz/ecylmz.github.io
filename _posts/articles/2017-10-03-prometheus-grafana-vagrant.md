---
layout: post
title: "Prometheus Grafana Vagrant"
modified:
categories: articles
excerpt:
tags: [prometheus, grafana, vagrant]
comments: true
share: true
---

Prometheus ve Grafana'yı test edebilmek için bir Vagrantfile hazırladım.

Depo: [https://github.com/ecylmz/prometheus-playground](https://github.com/ecylmz/prometheus-playground)

Depo dizininde `vagrant up` komutu tüm sistemi hazırlamaya yetiyor.

Grafana için 3 farklı dashboard'u provision aşamasında import ettim.
Dolayısıyla bunun için de ekstra uğraşmaya gerek yok.

Prometheus Dashboard: http://192.168.50.5:9090

Grafana Dashboard: http://192.168.50.5:3000  
Grafana kullanıcı giriş bilgileri:  
user: admin | password: admin

Prometheus Version: 1.7.2  
Grafana Version: 4.5.2

### Ekran Görüntüleri

Node Full Exporter:

![node-full-exporter](http://ecylmz.com/file/grafana-node-exporter-full.png)

Node Exporter Single Server:

![node-exporter-single-server](http://ecylmz.com/file/grafana-node-exporter-single-server.png)

Host Stats:

![host-stats](http://ecylmz.com/file/grafana-host-stats.png)
