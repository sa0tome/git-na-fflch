# git-na-fflch
Repositório para exercitar nossos conhecimentos em git na FFLCH

## Exercício 1: fazer um fork e clonar o repositório para a máquina local

1. Faça um fork desse repositório para o seu perfil
2. Insira o seu repositório (fork) na sua máquina local
3. Configure o `git remote`

```sh
git remote add origin <url-do-seu-fork>
git remote add upstream <url-da-upstream>
```

Exemplo

```sh
git remote add origin git@github.com:fulano/git-na-fflch.git
git remote add upstream git@github.com:sa0tome/git-na-fflch.git
```

Verifique se está correto

```sh
git remote -v
```

Deve ter como saída algo parecido com

```sh
origin  git@github.com:fulano/git-na-fflch.git (fetch)
origin  git@github.com:fulano/git-na-fflch.git (push)
upstream        git@github.com:sa0tome/git-na-fflch.git (fetch)
upstream        git@github.com:sa0tome/git-na-fflch.git (push)
```

## Exercício 2: desenvolver uma feature `olamundo` e enviar para seu fork

1. Crie um programa `olamundo` qualquer

Exemplo (bem besta, acho que vocês podem fazer melhor)
- criar um arquivo chamado `olamundo.txt`

2. Com o comando `git status`, conseguimos verificar o status geral do seu projeto. Provavelmente ele te informará que há um arquivo novo chamado `olamundo.txt` que ainda não foi versionado.
3. Vamos adicionar esse arquivo para ser versionado. Primeiro, adicione-o na *staging area* com o comando `git add olamundo.txt` e repita o comando `git status` para verificar se o arquivo foi adicionado.
4. Vamos registrar essa versão do projeto com o comando `git commit -m "<insira sua mensagem de commit>"`
5. Ao registrar essa versão do projeto, tenha em mente que esse registro foi local. Portanto, o seu fork no GitHub ainda não foi atualizado com suas mudanças. Para isso, vamos entrar o comando `git push origin master`

## Exercício 2: desenvolver uma feature `olamundo` e enviar para a upstream
1. Ao entrar no seu fork, automaticamente o GitHub irá comparar seu projeto com a upstream e vai te sugerir criar um *pull request*.
