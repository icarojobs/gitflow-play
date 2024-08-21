# gitflow-play

```bash
sudo apt install git-flow

# Inicialize o gitflow (1x por projeto) e responda algumas perguntas...
git flow init
> [basta dar enter para todas as perguntas] - usar o default

# Criar novo recurso (feature)
git flow feature start DBS-XX-criar-readme

# O comando acima cria um novo branch chamado 'feature/DBS-XX-criar-readme', baseado 
# no branch 'develop'. Ele também já faz o checkout pra esse novo branch.

# Commits (conventional commit)
git add file-name  (ou .)
git commit -m "feature(DBS-XX): add readme file"
git commit -m "feat(DBS-XX): add changelog"

# Ao finalizar sua task (boa prática), publique o seu branch e abra o PR:
git flow feature publish DBS-XX-criar-readme

# ATENÇÃO!!!
# Em algumas empresas você NÃO USA o comando para finalizar a feature:
git flow feature finish DBS-XX-criar-readme # CUIDADO!!!

# Geralmente, aguarda-se aceitar a PR, ai você simplesmente da um
git pull # na branch 'develop'
```

### Gitflow - Finalizando uma feature (NÃO APLICÁVEL EM ALGUMAS EMPRESAS)

Atualmente, os seus branches vão estar assim:

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/3c8efb15-4e26-4f04-84a4-396355713771/869db022-3fdf-438f-a4e4-e8c249734a0c/image.png)

Caso queira finalizar, basta digitar:

```bash
git flow feature finish DBS-XX-criar-readme

# Após digitar esse comando:
# 1. O branch 'feature/DBS-XX-criar-readme' é mergeado no branch 'develop'
# 2. O branch 'feature/DBS-XX-criar-readme' é excluído localmente
# 3. Você voltará automaticamente para o branch 'develop'
```

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/3c8efb15-4e26-4f04-84a4-396355713771/0e0a07e8-fadd-4a7d-ba32-066da623bd94/image.png)

Bastaria pushar o branch develop (mas não é uma boa prática já que, geralmente, o branch develop também pode ser usado em ambientes de homologação).

- O ideal é sempre pushar o branch `DBS-XX-nome-da-tarefa` para a origin e abrir uma nova PR.

### Tipos de flows (branches):

```bash
# Para criação de novos recursos
git flow feature start DBS-XX-nome-da-tarefa

```
