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
3. Vamos adicionar esse arquivo para ser versionado. Primeiro, adicione-o na *staging area* e vamos verificar se o arquivo foi adicionado.

```sh
git add olamundo.txt
git status
```

4. Vamos registrar essa versão do projeto:

```sh
git commit
```

Não se esqueça das [boas práticas](https://cbea.ms/git-commit/) para escrever sua mensagem de commit!

5. Ao registrar essa versão do projeto, tenha em mente que esse registro foi local. Portanto, o seu fork no GitHub ainda não foi atualizado com suas mudanças. Para atualizar seu repositório remoto entre com o comando:

```sh
git push origin master
```
## Exercício 3: enviar a feature `olamundo` para a upstream

Entre no seu fork no GitHub. O próprio site vai comparar seu fork com o upstream e vai te sugerir que você envie um *pull request*. Escreva detalhadamente as mudanças que você fez no projeto e solicite a inserção da sua feature na upstream com o *pull request*. Depois que os analistas revisarem seu código, nós vamos (ou não) autorizar o merge :)

## Exercício 4: atualizar as mudanças da upstream

0. Pode ser que você tenha mudanças no seu fork que você ainda não copiou para sua máquina local. Então, primeiro atualize sua máquina local com as mudanças do seu fork:

```sh
git fetch origin master
git merge origin/master
```

1. Atualizar as mudanças na sua máquina local

```sh
git fetch upstream master
git merge upstream/master
```

2. Subir essas mudanças para seu fork

```sh
git push origin master
```
