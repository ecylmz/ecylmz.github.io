---
layout: post
title: "Sunucuya Ağ Kablosu Bağlı mı?"
modified:
categories: articles
excerpt:
tags: [server, network, how-to]
comments: true
share: true
---

eth0'a kablo bağl mı?

```
# cat /sys/class/net/eth0/carrier 
1
```

1'in anlamı eth0'a fiziksel olarak bağlı bir kablo var.

peki eth1'e kablo bağlı mı?

```
cat /sys/class/net/eth1/carrier 
cat: /sys/class/net/eth1/carrier: Invalid argument
```

eth1'in down durumda olduğunu belirtir. Emin olalım:

```
# cat /sys/class/net/eth1/operstate 
down
```

Kablonun bağlı olup olmadığını test etmek için arayüzü ayağa kaldırmak gerekir:

```
# ifconfig eth1 up
```

Şimdi bakalım kablo durumuna:

```
# cat /sys/class/net/eth1/carrier 
0
```

0'ın anlamı eth1'e fiziksel kablo bağlı değil.

