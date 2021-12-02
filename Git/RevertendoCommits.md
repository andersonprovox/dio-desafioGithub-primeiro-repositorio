# Revertendo commmits
Nessa parte de reverter commits são vários que podem fazer a mesma coisa, por isso ter atenção em qual caso deve ser usado, ter muita atenção também porque este é um modo em que dependendo do cenário pode ser que o trabalho de alguém seja destruído ao reverter algum commit efetuado.

##  git reset

O git reset tem alguns meios pelo qual pode ser revertido um commmit

Reverter um commit pelo seu hash (SHA1):
```
git reset 8c6gf1
```

Reverter um commit pelo último apontado pelo tag HEAD:
```
git reset HEAD~1
```

Revertendo pela Tag HEAD, veja que o número depois do til, é o total de commits que devem ser revertidos, aqui no exemplo diz que pegue o local em que está a tag HEAD apontada e mova para o anterior. Se fosse outro número imagine que seria x commits atrás.

Para fazer um reset de apenas uma casa podemos usar:
```
git reset --soft
```

Mas sabendo quantos commits quer reverter:
```
git reset --soft HEAD~1
```

Para fazer com que o último commit seja retirado até da staging area está da qual é adicionado o arquivo após o `git add` então use o `--mixed`.
```
git reset --mixed HEAD~1
```

**Ponto de atenção:** qualquer comando que use o atributo `--hard`, `--force` ou `-f` deve tomar cuidado pois esses fazem com que seja destruído ou excluído o arquivo com código escrito.
```
git reset --hard HEAD~1
```

## Git revert
O git revert ele não faz a alteração do arquivo ou das mudanças no commit, faz apenas o apontamento ou movimentação para determinados commits. O que ele faz é reverter a alteração de um determinado commit criando um novo, desfazendo alterações e/ou adições de arquivos do commit apontado.

Usa os conceitos de apontamento do `git reset`.
```
git revert HEAD~1

git revert 8fs7lxc1
```





