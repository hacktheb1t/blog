+++
title =  "Fazendo uma manutenção básica no Windows"
date =   2020-08-02T13:00:00Z
draft = false
+++

Neste post você vai aprender como fazer uma manutenção simples no seus dispositivo com Windows instalado.

**Verificação de disco**

O primeiro passo para este processo é verificar se o seu HD ou SSD estão funcionando corretamente, pois problemas relacionados ao disco causam lentidão ao seu sistema.

Se seu disco não estiver funcionando corretamente, mesmo que haja uma formatação e reinstalação do Windows, este por sua vez continuará lento, ou então o problema já pode vir de fábrica, isto infelizmente acontece.

Para fazer isto é necessário instalar o Western Digital Data Lifeguard para fazzer esta verificação que pode ser utilizado para qualquer dispositivo de outras fabricantes.

Quando instalado execute o Extended Test para fazer uma verificação completa no disco, este processo pode demorar várias horas dependendo da capacidade do seu disco, como este é um processo complexo, não o interrompa, pois pode causar erros no seu disco. No final do processo haverá um icone indicando o estado do seu disco, se for um ícone verde com formato de v quer dizer que seu disco está bem, caso o programa detecte um erro mostrará outro ícone que vai indicar que seu disco não é mais confiável e é nescessário trocá-lo.

O próximo passo é corrigir os arquivos do Windows. Este processo verifica e corrige seus arquivos corrompidos, caso tenha.

O programa que será usado é nativo do Windows, não sendo nescessário baixa-lo, outro lembrete é que ele pode ficar parado por um tempo considerável pode levar a entender que ele travou, no entanto ele na verdade encontrou um arquivo corrompido e esta em processo de correção que é bem lento. Outra observação é que esta tarefa pode levar até 12 horas e que não pode ser interrompida de modo algum.

Para executar o programa clique com o botão direito do mouse no logotipo do Windows, abrirá uma janela, clique em Prompt de comandos ou Windows PowerShell (Admin), assim que abrir uma janela de confirmação clique em "sim". Em seguida digite este comando e clique enter:

```bash
chkdsk /R
```

Depois confirme com "S" e enter para fazer a verificação na reinicialização do Windows. Reinicie o seu sistema e espere a verificação completa do seu disco.

Quando o Windows iniciar normalmente faça os mesmos passos anteriores para abrir o Promp de Comando ou PowerShell (Admin),  em seguida digite este comando e clique enter:

```bash
sfc /scannow
```

Ele vai verificar e reparar os arquivos protegidos do Windows, este processo é mais rápido que os anteriores.

A ultima parte deste processo de verificação de disco é usar o DISM, ainda no terminal do Windows digite este comando e enter:

```bash
DISM /Online /Cleanup-image /Restorehealth
```

Este comando não funciona no Windows 7, este programa repara arquivos corrompidos ou ausentes no seu sistema.

**Limpeza de disco**

Confrome se utiliza o sistema Windows, vão se acumulando arquivos temporários nele e se este não forem apagados de com certa frequência eles acabam ocupando muito espaço de disco e ocasionar problemas no desmpenho do seu Windows.

Para isto no momento da publicação deste post é a utilização de um programa de terceiro chamado CCleaner, por fazer uma limpeza destes arquivos principalmente em navegadores, pois geralmente estes costumam acumular bastante aruivos temporários.

Inicialmente busque no seu sistema o programa "Limpeza de Disco", selecione o disco que vai ser limpo, geralmente para usuários comuns é o disco "C:", clique em OK, clique em limpar arquivos do sistema, o programa irá reiniciar, clique novamente no disco que será limpo e clique em OK, clique em mais opções e clique em Limpar no quadro com "Restauração de Sistema e Cópias de Sombra", clique em excluir, depois clique em limpeza de disco e selecione tudo ali, com ressalvas a pasta de Downloads, pois possivelmente pode ter arquivos importantes nela, continue clicando em OK e a limpeza será feita.

Agora execute o CCleaner e feche todas as janelas de navegadores, com ele aberto clique em analize, depois de analisar os navegadores clique em run ccleaner e espere a remoção dos arquivos temporários dos seus navegadores.

**Remoção de Bloatwares**

Bloatwares são programas pré--instalados no seu sistema e que podem ser responsáveis pela lentidão do seu Windows, além disto, pode tornar o Windows instável e inseguro.

Para isto  é nescessaŕio instalar o programa PC Decrapifier que identifica e remove estes programas.

Este processo é bem simples, execute o programa, clique em analize, depois serámostrado quais os programas identificados, em seguida clique neles e clique em remover.

Além deste programa existe outro  chamado de AdwCleaner da Malwarebytes.

**Remoção de Adwares e PUPs**

Adwares são programas que mostram propagandas indesejadas no seu sistema tentando enganar o usuário para clicar nela para comprar algo desnescessário ou infectar a máquina deste mesmo usuário. O PUP é um programa que vem instalado junto com outro que você escolheu instalar. Geralmente sites com Baixaki, Superdownloads, etc, continuam utilizando estes programas para aumentar sua receita, por isto é sempre recomendado baixar programas do seu próprio site oficial.

Para fazer isto executamos o AdwCleaner da Malwarebytes sitado anteriormente para fazer esta remoção. 

Assim que iniciado vá em configuraçoes e mude a linguagem para Português, em seguida volte ao Painel e clique em "Verificar Agora", no final ele irá mostrar os programas que ele identificou, depois clique em "Quarentena"  e depois em "continuar",  assim que terminar o programa irá pedir para reiniciar seu sistema, reinicie depois volte nele e clique em "Quarentena" selecione todos e clique em "Eliminar".

Além disso desinstale todos os programas que se dizem otimizadores do sistema, eles geralmente são da Ashampoo, Baidu, GlarySoft, IObit, Wisecleaner, alem de programas que venham no nome Optmizer, Tuneup, Speed, etc. Estes programas que geralmente são instalados por técnicos em informática são totaçmente desnecessários e atrapalham o funcionamento do Windows.

**Eliminação de Malwares**

Embora seu computador já venha com antivírus, é possível que este não seja tão eficiente e a melhor maneira de garantir que o seu sistema esta limpo destes malwares é uma verificação com outros antivírus, pois cada um tem maneiras diferentes de verificação de um malware. Neste processo iremos utilizar três antivírus diferentes em suas versões de varredura online, caso algum malware seja detectado neste processo, isto é um sinal que ele deva ser trocado por outro melhor, neste caso a recomendação mais frequente são é do Kaspersky Security Cloud Free ou sua versão paga.

A primeira varredura usaremos o TrendMicro HouseCall, baixe e execute-o, siga o processo de inicialização, depois abrirá uma tela para scanear seu sistema, nela clique em settings e marque a opção Full system scan, clique em Ok e faça o scaneamento do sistema. No final do processo, caso ele tenha detectado algo de errado ,clique em "FixNow" para finalizar o processo.

A segunda usaremos o KVRT(Kaspersky Virus Removal Tool), baixe e execute-o, siga o processo de inicialização do programa, depois clique em "Change parameters" e selecione em  system drive garantindo a varredura completa do seu sistema, depois "StartScan", no final elimine todas as ocorrências de malware.

O ultimo será o ESET Online Scanner, baixe e execute-o, siga o processo de inicialização do programa aceitando somente a licença, depois faça o escaneamento completo clique na primeira opção que coloca tudo que for detectado em quarentena e inicie a varredura, no final da varredura ele pode pedir para continuar no seu sistema, é bom que não continue, pois é melhor ter um antivírus instalado da maneira padrão.

Depois de fazer estas três varreduras é certeza que seu sistema esta limpo de malwares. Lembrando que, caso eles tenham detectado algum malware, é recomendado a instalação de outro antivírus.

**Bloqueador de Propagandas de de URL**

O motivo desta parte é simplesmente para bloquear banners que podem conter códigos maliciosos, e isto pode acontecer independente do site que é acessado.

Para isso é recomendado o uso do uBlock Origin que é uma extensão de navegador que pode ser usado no Chrome, Firefox e Edge. Para instala-lo, clique no botão de configurações do navegador, representado com três pontinhos, vá em "mais ferramentas" e clique em "Extensões", depois clique em abrir chrome webstore, pesquise por ublock origin e instale-lo. Além de ficar mais seguro sua navegação será mais rápida.

O bloqueador de URLs vai bloquear sites que são conhecidos como maliciosos, além de bloquear sites falsos utilizados para phising. Para insto existe o Kaspersky Protection que tambem é uma extensão que funciona no Chrome, Firefox e Edge, outra extensão recomendada é o TrafficLight da bitdefender.

**Desfragmentação de arquivos**

Embora o Windows tenha seu próprio desfragmentador, é recomendado o uso da versão gratuita do Defraggler, baxe-o do site oficial, desclique qualquer instalação de software adicional e instale-o.

Para configurá-lo clique em configurações -> mapa do dispositivo -> visão customizada, selecione 12 e 12, estilo plano e modo barras, clique em OK, depois volte em configurações -> desfragmentar e clique em mover arquivos grandes e como tamanho mínimo coloque 1000, clique em OK.

Depois clique na aba saúde e saberá se seu disco tem algum problema, caso tenha algum problema é recomendado fazer backup dos arquivos e comprar um novo disco, pois este não é mais confiável.

Para iniciar a desfragmentação, clique em configurações -> Desfragmentar na inicialização -> Executar uma vez e depois clique em não, depois sem ter reiniciado, clique antes em desfragmentar, depois reinicie.

**Dicas Extras**

Feito todo este processo, seu sistema esta pronto para o uso seguro, para que continue assim é necessário algumas boas práticas.

A primeira delas é deixar habilitado o Windows Update e sempre atualizar seu sistema, geralmente, nessas atualizações sempre vem correções de segurança ou estabilidade, te previnindo de futuros erros ou infecções. Esta dica também serve para seu antivírus, especialmente se for a versão paga.

Executar o CCleaner e o Defraggler, comentados anteriormente,  a cada 15 dias no máximo.

Cuidado com extensões do Chrome, algumas delas, mesmo que com nomes conhecidos podem ter atitudes maliciosas.

Nunca utilize cracks e ativadores para piratear programas pagos, pois todos eles possuem malwares recém-criados que muitas vezes não são detectados pelos antivírus. Esta é uma dica tambem para nunca ativar o Windows de forma pirata, pois pode ser pior causando a famosa tela azul, para isso, caso não queira comprar uma nova key do Windows, o sistema aceita keys de ativação de seu sistema anterior, keys do Windwos 7 e 8 funcionam no 10.
