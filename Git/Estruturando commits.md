# Estruturando commits
Melhorar e fazer uma boa estruturação dos commits que faz num repositório aonde você e outras pessoas vão usar, traz os seguintes benefícios:

- Melhor legibilidade do histórico
- Amigável para novos desenvolvedores
- Amigável ao versionamento semântico

## Commits atômicos

Um commit atômico mantém a unidade da alteração que foi feita em seu código por exemplo, se você alterou o footer da página, deixe um commit com tudo que foi alterado no footer, se mexeu no menu lateral deixe somente o menu lateral dentro de um commit, com essa recomendação tudo que é de competência de uma parte deve ser agrupado dentro de um commit.

## Português x Inglês

Se o commit vai ser em português ou inglês isso vai depender do contexto no qual a empresa está, se é uma empresa multinacional com projeção internacional e que quer ou precisa de seu código seja utilizado por profissionais de outra língua então escrever em inglês faz sentido.

## estrutura do commit

- Assunto
- Corpo
- Rodapé

**Assunto**: Curto e compreensivel até 50 caracteres, começar sempre com letra maúscula, Não terminar em ponto, escrever de forma imperativa.

A forma imperativa assim como no inglês podemos escrever no português, apesar que acho que para o português a ideia é que fique no infinitivo, mas aí é mero detalhe.

Em inglês:
add a feature, add, footer, replace main etc

Em português:
adiciona a funcionalidade x, modifica uma funcionalidade existente, etc.

Se aceito esse commit...(só adicionar uma das frases de exemplo acima).

**Corpo**: adicione detalhes ao commit, tente quebrar a linha em 75 caracteres, identifique a sua audiência, explique tudo, use Markdown.

**Rodapé**: referencia assuntos relacionados

Para conseguir inserir comentários mais detalhados no commit use o comando sem o `-m`.

```
git commit
```

## Commits semânticos
A especificação Conventional Commits é uma convenção simples para utilizar nas mensagens de commit. Ela define um conjunto de regras para criar um histórico de commit explícito, o que facilita a criação de ferramentas automatizadas baseadas na especificação. Esta convenção se encaixa com o SemVer, descrevendo os recursos, correções e modificações que quebram a compatibilidade nas mensagens de commit. [link](https://www.conventionalcommits.org/).

### Versionamento semântico
Programas possuem versões e sua numeração indica que versão está.
mais [Informações](https://semver.org).





