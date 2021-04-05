+++
title =  "FTP Enumeration"
date =   2020-07-10T15:00:00Z
draft = false
+++

Estas são algumas dicas para fazer uma enumeração de um serviço FTP.

### FTP Syntax
Se um serviço FTP for encontrado, tente uma conexão anônima como 'anonymous' ou 'ftp'.
### Liste arquivos escondidos
Use 'ls' com o arqumento '-a'.
### Transferindo binários
Para transferir binários você deve dar o comando 'bin' no server alvo. 
### Download de todos os arquivos recursivamente
Para clonar o diretório inteiro  você deve setar na hora do acesso via FTP, você pode usar o '-m' mirror option, ou use o '-r' recursive option.
```bash
root@kali:~# wget -r --no-passive ftp://(USERNAME):(PASSWORD)@(TARGET IP ADDRESS)
```
