---
layout: post
title:  "Comandos no nmap"
date:   2020-07-10
---
O nmap é um scanner de portas para reconhecimento de um alvo.

Comando básico
```bash
nmap 192.168.1.150
```

Obtendo mais detalhes de um endereço
```bash
nmap -v 192.168.1.150
```

Varedura de uma rede utilizando Wildcards
```bash
nmap 192.168.1.*
```

Wildcards e excluindo alguns ips
```bash
nmap 192.168.1.* --exclude=192.168.1.200
```

Utilizando um arquivo com uma lista de IPs
```bash
nmap -iL lista-ips.txt
```

Descobrir o Sistema Operacional e o Traceroute de determinado IP
```bash
nmap -A 192.168.1.150
```

Descobrir o Sistema Operacional de determinado IP com mais detalhes e mais organizado
```bash
nmap -O 192.168.1.150
```

Verificar se um firewall está protegendo
```bash
nmap -PN 192.168.1.150
```

Enganar o firewall
```bash
nmap -sN 192.168.1.150
```

Usando script
```bash
nmap -sC 192.168.1.150
```

Verificar sem fazer muito barulho na rede
```bash
nmap -sS iptarget
```

nmap versão gráfica zenmap
```bash
sudo [gerenciador] [install] zenmap
```
