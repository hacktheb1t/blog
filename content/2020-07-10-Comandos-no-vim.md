+++
title =  "Comandos no vim"
date =   2020-07-10T14:00:00Z
draft = false
+++

O VIM e um editor de texto mais famoso entre os programadores, alguns odeiam, outros amam porque esta ferramenta e poderosa, porem um pouco complexa para quem prefere usar interfaces gráficas ouo mouse para tudo. Este artigo serve para quem tem curiosidade de conhecer esta ferramenta.

O vim tem suporte a expressões regulares e a mais de 500 linguagens, nele tambem tem corretor ortográfico a partir da versao 7.0.

Agora estão aqui alguns comandos básicos do vim:

vim | abre arquivo vazio
vim arquivo.txt | abre o arquivo.txt, caso este arquivo não exista, ele cria um
vim arquivo.txt + | abre o arquivo.txt com o cursor no final do arquivo
vim arquivo.txt +10 |  abre o arquivo.txt com o cusor na linha 10, por exemplo
vim arquivo.txt +/exemplo | abre o arquivo.txt na com o cursor na primeira ocorrencia da palavra exemplo
vim -o arq1.txt arq2.txt ... | abre multiplos arquivos em paralelo na disposicao de colunas horizontais
vim -O arq1.txt arq2.txt ... | abre multiplos arquivos em paralelo na disposicao de colunas verticais

O vim tem vários modos para a edição de texto:

ESC | Entra em modo de comandos
i | Entra em modo de inserção para comecar a escrever
: | Serve para indicar alguma modificação do arquivo
v | selecao visual do texto
/ | Busca de padrões no texto
R | Reposição de texto

Entre estes modos existem alguns comandos:

**OBS**: Para entrar no modo de comandos e necessário sempre clicar em [ESC].

Com modo ':':

:q | para sair
:q! | para sair forçado
:w | para salvar alterações
:wq ou :x ou :ZZ | para salvar e sair
:wa | salva todos os arquivos abertos
:wqa | para salvar e sair de todos os arquivos abertos
:split [arquivo/caminho-do-arquivo] | abre um novo arquivo exixtente ou não na posição horizontal
:syntax on | ativa a cor de sintaxe de uma linguagem

Outros comandos:

crtl ww | quando se abre multiplos arquivos com este comnado pode-se mudar de um texto para outro
a	|	você pode inserir após a posição do cursor
o	|	insere texto em uma nova linha abaixo de onde o cursor estiver posicionado
r	|	insere sobrescrevendo
k	|	Serve como tecla direcional para cima
l	|	Serve como tecla direcional para direita
h	|	Serve como tecla direcional para esquerda
j	|	Serve como tecla direcional para baixo
v	|	marca a linha/texto onde o cursor esta posicionado e com as teclas direcionais seleciona até o ponto desejado
shift+v	|	seleciona visualmente todo o parágrafo
y | após selecionado com v e feita a copia do texto selecionado
d | recorta o texto seleciona com v ou a linha sem v
p | cola o texto apos ser copiado ou recortado
yy | copia a linha inteira
5yy | copia ate cinco linhas abaixo contando com a linha do cursor esta posicionado
ggVG | seleciona tudo
dd | deleta toda a linha onde o cursor estiver posicionado
u | desfaz as alterações feitas
$ | vai para o fim da linha
^ | vai para o início da linha
:$ ou G | vai para o fim do arquivo
gg | vai para o início do arquivo
:5 ou 5G | vai para a quinta linha
w | pula para a próxima palavra
b | pula para a palavra anterior
( | pula para a frase anterior
) |pula para a próxima frase
{ | pula para o parágrafo anterior
} | pula para o próximo parágrafo
/exemplo | busca a palavra exemplo

Dicas:

ESC :set backspace | o vim habilita o backspace caso a sua versão não suporta o backspace
ESC :set nu! | enumera as linhas do arquivo
ESC :1,10w arq.txt | salva da linha 1 a linha 10 do arquivo atual
ESC :map ggVG? | mapeia a tecla F12 para selecionar tudo
ESC :%s//NADA/ | troca a 1 ocorrência de '' por 'NADA'
ESC :%s//NADA/g | troca todas as ocorrência de '' por 'NADA'
ESC :%s//NADA/gc | troca as ocorrências de '' por 'NADA' pedindo confirmação
ESC :set textwidth=90 | limita digitação ate a coluna de número 90
ESC :u | converte para minúsculas apos texto selecionado com v
ESC :U | converte para maiúsculo apos texto selecionado com v

Linha de comando:

Tambem e possível executar comandos do vim pelo terminal apenas acrescentando '-c'.

Exemplo:

```bash
vim -c ":%s/palavra/outra/g" -c ":x" arquivo.txt
```

O VIM tem a possibilidade de estender suas funcionalidades para maior produtividade com plugins.
