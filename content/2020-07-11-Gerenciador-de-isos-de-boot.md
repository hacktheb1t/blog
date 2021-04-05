+++
title =  "Gerenciador de isos de boot"
date =   2020-07-11T13:00:00Z
draft = false
+++

A aplicação em questão que vamos falar um pouco e o Ventoy. Este aplicativo e bem simples de se utilizar, ele simplesmente ajuda a ter várias isos de sistemas operacionais em um único pendrive sendo necessário apenas copiar a imagem da iso e colar no pendrive com o Ventoy.

Ele pode ser encontrado no link do seu próprio [site](https://www.ventoy.net) do Ventoy e seus comandos são bem simples para fazer a instalação no seu pendrive.

Para fazer a instalação no pendrive desejado e necessário o seguinte comando:

```bash
$ sudo ./Ventoy2Disk.sh -i /dev/[SeuDispositivo]
```

Caso queira o modo persistente no pendrive

```bash
$ sudo ./CreatePersistentimg.sh -i /dev/[SeuDispositivo]
```

Também pode habilitar o secure boot no pendrive

```bash
$ sudo ./Ventoy2Disk.sh -i -s /dev/[SeuDispositivo]
```

Depois deste processo seu pendrive será dividido em duas partições, uma com a aplição e outra para colar suas isos.

