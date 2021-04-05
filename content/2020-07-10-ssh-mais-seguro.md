+++
title =  "Ssh mais seguro"
date =   2020-07-10T16:00:00Z
draft = false
+++

Para um uso mais seguro do ssh e recomendado o uso destas configurações no arquivo sshd_config em /etc/ssh/. Neste arquivo deve-se apenas descomentar as linhas:

1 - mudar a porta do ssh

```sh
Port 1234
```

2 - mudar o ClientAlive para que a sessão de usuário ssh logado tenha um tempo de inatividade e que tenha um limite de usuários ativos

```sh
ClientAliveInterval 360 
ClientAliveCountMax 1
```

3 - não permitir senha vazia

```sh
PermitEmptyPasswords no
```

4 - não permitir o login direto no usuário root

```sh
PermitRootLogin no
```

5 - não permitir acesso por senhas, e mais seguro entrar com chaves RSA. Lembrando que somente deve ser habilitada esta propriedade quando as chaves ja estiverem configuradas na máquina remota

```sh
PasswordAuthentication no
```

Depois reinicie o serviço ssh

```bash
/etc/rc.d/rc.sshd restart
```
ou
```bash
/etc/init.d/ssh restart
```
