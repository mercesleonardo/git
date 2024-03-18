## Readme Completo do Git: Dominando Branches e Merge

**Introdução:**

Este guia detalhado irá te levar do básico ao avançado no uso de branches e merge no Git. Aprenda a criar, gerenciar e integrar branches com segurança e eficiência.

**Pré-requisitos:**

* Ter o Git instalado e configurado em seu computador.
* Familiaridade com os comandos básicos do Git (commit, push, pull, etc.).

**Conteúdo:**

**1. Verificação da Existência da Branch "Developer":**

```bash
git branch -l
```

**2. Mudança para a Branch "Developer":**

```bash
git checkout developer
```

**3. Criação de uma Nova Branch:**

```bash
git checkout -b <nome-da-sua-nova-branch>
```

**4. Envio de Branches para o Repositório Remoto:**

```bash
git push origin <nome-da-sua-branch>
```

**5. Atualização de Branches Locais:**

**5.1 Usando `git fetch`:**

```bash
git fetch origin
```

**5.2 Usando `git pull`:**

```bash
git pull origin <nome-da-branch>
```

**6. Visualização de Branches:**

```bash
git branch
```

**7. Realização de Merge:**

**7.1 Integração de uma Hotfix:**

* Navegar para a branch `developer`:

```bash
git checkout developer
```

* Verificação da atualização da branch `hotfix/SERV04/v0.0.1`:

```bash
git fetch origin
```

* Merge da branch `hotfix/SERV04/v0.0.1` na branch `developer`:

```bash
git merge origin/hotfix/SERV04/v0.0.1
```

* Resolução de conflitos de merge (se houver).

* Verificação do sucesso do merge:

```bash
git status
```

* Empurre a branch `developer` para o repositório remoto:

```bash
git push origin developer
```

**Dicas Extras:**

* Use nomes descritivos para suas branches.
* Crie branches para cada nova tarefa ou feature.
* Faça merges frequentemente.
* Utilize ferramentas visuais como o SourceTree ou o GitKraken.

**Conclusão:**

Este guia te forneceu uma base sólida para dominar o uso de branches e merge no Git. Com prática, você será capaz de gerenciar seus projetos de forma eficiente e colaborar com outros desenvolvedores com facilidade.

