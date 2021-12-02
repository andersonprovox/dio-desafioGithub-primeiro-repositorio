# Visualização de histórico
o comando para verificar em que branch está:
```
git branch
```

Quando ver um asterisco ao lado do nome das branches listadas então é nesta branch que está localizado e todo commit feito será vinculado à essa branch.

## Alterando o nome de uma branch
É possível fazer a alteração do nome de uma branch tanto dentro dela mesma, como a partir de uma outra branch.

dentro da branch:

```
git branch -m novo_nome
```

Trocando o nome de uma branch através de uma outra já selecionada:
```
git branch -m nome_atual novo_nome
```

Deletando uma branch
```
git branch -d nome_branch
```

## Evitando carregar sujeita entre branches
Quando acontece a mudança entre branches e que é corriqueiro no dia a dia, após um commit você pode carregar esses arquivos para a nova branch, para que não vire bagunça é importante colocar esses arquivos dentro de um **stash**.

### Stash
O _stash_ pega todos os seus arquivos que estão na área de _staging area_, isso é a quela área que ficam os arquivos após o _commit_ e os coloca dentro de uma caixinha(simbolicamente falando) e evita que você carregue esses arquivos se for trabalhar em uma nova _branch_ com arquivos de uma outra completamente diferente.

Para criar um stash antes de mudar de branch.
```
git stash save "seu comentário"
```

O _stash_ quando usado vários salvamentos cria uma lista ou um _array_ de salvamentos, quando você salva um _stash_ ele te informa após salvar o nome da _branch_ ao qual foi salvo aquele slot de arquivos e o comentário inserido para identificação da alteração salva no _stash_.

Após usar o comando stash a sua área de commit estará limpa, assim pode mover para a outra branch e continuar o seu trabalho.

Um detalhe é que o array se comporta como uma lista First In Last Out sempre o seu último save será estará no índice 0 (zero).

Para resgatar um trabalho no stash e retorno o que foi interrompido:

```
git stash pop <número do índice do stash>
```

Caso não saiba e queira listar todos os stash salvos:
```
git stash list
```

Caso seja necessário limpar o stash:
```
git stash clear
```

## Git log

O comando git log faz com que visualize o histórico cronológico de commits.

```
git log
```

O comando acima tem a característica de ser genérico e com isso traz muita informação de todos os commits no repositório.

para verificar o histórico de arquivos commitados em um diretório do repositório:

```
git log nome_do_diretorio
```

Ver o histórico de um arquivo específico:
```
git log nome_do_arquivo
```

Exibir o histórico de commits de forma resumida em uma linha:
```
git log --oneline
```

Forma gráfica de como ver o commit das branches
```
git log --graph
```

De uma forma mais gráfica no windows:
```
gitk
```

Há ferramentas gráficas para Linux, lá você pode escolher a que você quer usar.
