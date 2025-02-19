# Guia de Instalação e Configuração do GIT

Este guia cobre os passos para instalar, configurar e utilizar o GIT em um repositório. Siga as instruções abaixo para começar.

## 1. Instalação do GIT

Siga as etapas do [site oficial do GIT](https://git-scm.com) para instalar o GIT no seu sistema.

## 2. Configuração do GIT

Após a instalação, é necessário configurar seu nome e e-mail para que as alterações sejam registradas corretamente. Para isso, execute os seguintes comandos no terminal (Git Bash, por exemplo):

```bash
git config --global user.name "Joe Doe"
git config --global user.email "acme@acme.com"
```

Essas configurações são importantes para identificar as alterações feitas por você no repositório.

## 3. Fluxo de Utilização

Após configurar o GIT, você pode começar a usar em seus projetos. Abaixo estão os principais comandos para trabalhar com repositórios Git.

### 3.1 Inicializando um Repositório

Para iniciar um novo repositório Git em um diretório, use o comando:

```bash
git init
```

Esse comando cria um repositório Git vazio no diretório atual, permitindo que você comece a versionar seu projeto.

### 3.2 Verificando o Status do Repositório

Após fazer alterações nos arquivos, você pode verificar o status atual do repositório com o seguinte comando:

```bash
git status
```

Isso mostrará o estado dos arquivos, como modificados ou não rastreados.

### 3.3 Estágios de Arquivos no GIT

Os arquivos em um repositório Git podem estar em diferentes estágios durante o processo de versionamento. São eles:

- `Untracked`: Arquivos que não são rastreados pelo Git ainda.
- `Modified:` Arquivos que foram alterados desde o último commit.
- `Staged:` Arquivos que foram preparados (staged) para o próximo commit.
- `Commit:` Arquivos que foram registrados no histórico do repositório com um commit.

Esses estágios ajudam a controlar as alterações e como elas serão incluídas no repositório.

### 3.4 Criando um Arquivo `.gitignore`

O `.gitignore` é um arquivo especial que define quais arquivos e diretórios devem ser ignorados pelo Git, ou seja, não serão rastreados nem adicionados ao repositório. Isso é útil para evitar que arquivos sensíveis, arquivos de configuração local e diretórios gerados automaticamente sejam versionados.

Dentro do arquivo .gitignore, você pode especificar arquivos e pastas que deseja ignorar. Exemplos:

```bash
# Ignorar arquivos compilados
*.log
*.out
*.class

# Ignorar diretórios específicos
node_modules/
dist/
venv/

# Ignorar arquivos de configuração local
.env
```

## 4. Realizando um Commit

Após realizar alterações no repositório e verificar o status, você pode adicionar arquivos ao estágio e realizar commits com os seguintes comandos:

```bash
git add <arquivo>
git commit -m "Mensagem do commit"
```

### 4.1 Comandos de Push e Pull

Após realizar commits locais, você pode sincronizar seu repositório local com o repositório remoto.

#### 4.1.1 Enviando Alterações para o Repositório Remoto (Push)

Para enviar suas alterações locais para um repositório remoto (por exemplo, no GitHub), você pode utilizar o seguinte comando:

```bash
git push origin <nome-da-branch>
```

#### 4.1.2 Buscando Alterações do Repositório Remoto (Pull)

Para trazer as alterações mais recentes do repositório remoto para o seu repositório local, você pode utilizar o seguinte comando:

```bash
git pull origin <nome-da-branch>
```

---

Para mais informações sobre comandos e fluxo de trabalho do Git, consulte a [documentação oficial](https://git-scm.com/doc).
