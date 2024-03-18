##  Guia Completo do Git: Dominando Branches e Merge

**Introdução:**

Este guia detalhado irá te levar do básico ao avançado no uso de branches e merge no Git. Aprenda a criar, gerenciar e integrar branches com segurança e eficiência.

**Pré-requisitos:**

* Ter o Git instalado e configurado em seu computador.
* Familiaridade com os comandos básicos do Git (commit, push, pull, etc.).

**1. Verificando a Existência da Branch "Developer":**

```bash
git branch -l
```

Este comando lista todas as branches existentes no seu repositório local. Se a branch "developer" estiver na lista, você pode seguir para a próxima etapa.

**2. Mudando para a Branch "Developer":**

```bash
git checkout developer
```

Este comando coloca você na branch "developer". A partir de agora, todas as suas alterações serão feitas nesta branch.

**3. Criando uma Nova Branch:**

```bash
git checkout -b <nome-da-sua-nova-branch>
```

Crie uma nova branch a partir da branch "developer" usando o comando acima, substituindo `<nome-da-sua-nova-branch>` pelo nome desejado para a sua nova branch.

**4. Enviando Branches para o Repositório Remoto:**

Após criar e fazer alterações em uma branch local, você precisa enviá-la para o repositório remoto para que outras pessoas possam acessá-la. Utilize o comando `git push`:

```bash
git push origin <nome-da-sua-branch>
```

Substitua `<nome-da-sua-branch>` pelo nome da branch que você deseja enviar.

**5. Efetuando Commits no Git

O commit é o processo de registrar as alterações feitas nos seus arquivos localmente no seu repositório Git. É uma prática essencial para manter um histórico de suas modificações e colaborar com outros desenvolvedores.

**Siga estes passos para realizar um commit no Git:**

1. **Adicione os arquivos que você deseja registrar ao índice de staging:**

```bash
git add <nome-do-arquivo>
```

Você pode adicionar vários arquivos de uma vez usando o seguinte comando:

```bash
git add .
```

Este comando adiciona todos os arquivos modificados no diretório atual ao índice de staging.

2. **Crie um commit com uma mensagem descritiva:**

```bash
git commit -m "Mensagem descritiva das alterações"
```

A mensagem do commit deve ser clara e concisa, resumindo as modificações que você está registrando.

3. **Verifique o histórico de commits:**

```bash
git log
```

Este comando irá mostrar o histórico de commits do seu repositório local, incluindo a mensagem de cada commit.

**6. Atualizando Branches Locais:**

**6.1 Usando `git fetch`:**

O comando `git fetch` é útil para verificar se há atualizações no repositório remoto sem integrar as alterações à sua branch local:

```bash
git fetch origin
```

Este comando irá baixar as últimas alterações do repositório remoto para o seu computador local, mas não irá mesclá-las com a sua branch atual.

**6.2 Usando `git pull`:**

O comando `git pull` é mais poderoso que o `git fetch`. Ele não apenas verifica se há atualizações, mas também as integra à sua branch local:

```bash
git pull origin <nome-da-branch>
```

Este comando irá baixar as últimas alterações da branch `<nome-da-branch>` do repositório remoto e mesclá-las com a sua branch local.

**7. Visualizando Branches:**

Para ver uma lista de todas as branches existentes em seu repositório, incluindo a branch atual, utilize o comando `git branch`:

```bash
git branch
```

A branch atual será marcada com um asterisco (*) ao lado do nome.

**8. Realizando Merge:**

**8.1 Integrando uma Hotfix:**

Suponha que você precisa integrar a branch `hotfix/SERV04/v0.0.1` na branch `developer`. Siga estas etapas:

1. Navegue para a branch `developer`:

```bash
git checkout developer
```

2. Verifique se a branch `hotfix/SERV04/v0.0.1` está atualizada:

```bash
git fetch origin
```

3. Faça o merge da branch `hotfix/SERV04/v0.0.1` na branch `developer`:

```bash
git merge origin/hotfix/SERV04/v0.0.1
```

4. Resolva qualquer conflito de merge:

Se o merge encontrar conflitos, você precisará resolvê-los manualmente. O Git irá te avisar sobre os arquivos que contêm conflitos e você precisa editar esses arquivos para mesclar as alterações de ambas as branches.

5. Verifique se o merge foi bem-sucedido:

```bash
git status
```

6. Empurre a branch `developer` para o repositório remoto:

```bash
git push origin developer
```

**Dicas Extras:**

* Use nomes descritivos para suas branches para facilitar a identificação.
* Crie branches para cada nova tarefa ou feature que você estiver trabalhando.
* Faça merges frequentemente para integrar suas alterações à branch principal.
* Utilize ferramentas visuais como o SourceTree ou o GitKraken para facilitar o gerenciamento de branches.
