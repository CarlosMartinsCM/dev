[Home](https://github.com/fscheidt/dev)

# Git

---

## Comandos

Lista de comandos frequentes:

### criar repositório git
```
mkdir myproject
cd myproject
git init
git add -A
git commit -m "initial commit"
```

### clonagem
Faz download de todo o projeto:
```
git clone https://github.com/fscheidt/dev.git
```

**Clonagem rasa:**

Obtém uma cópia do repositório com a última versão apenas (ignora histórico). Útil quando o repositório é muito grande.

```bash
git clone --depth 1 https://github.com/django/django.git
````

**Clonagem profunda:** ou duplicar o repositório, o que significa que todos os branchs vão ser copiados, não apenas o master/main.

```bash
git clone --bare https://github.com/github/gitignore
```


### push
**enviar** alterações para o servidor remoto
```
git push origin master
```

### pull
**baixar** alterações do servidor
```
git pull origin master
```

---

## gitignore
O arquivo `.gitignore` deve ser criado na pasta raiz do projeto. Nele são especificados os padrões de arquivos e diretórios que devem ser ignorados no controle de versionamento. A seguir alguns templates para o gitignore de acordo com a linguagem de desenvolvimento:

### Projetos python

Todos os arquivo a seguir serão *ignorados* pelo git:
```
*.zip
*.7z
.idea/

# Jupyter Notebook
.ipynb_checkpoints

__pycache__/  
*.py[cod]  
*$py.class

# Distribution / packaging
build/
develop-eggs/
dist/
downloads/
lib/

# Environments
.env
.venv
env/
venv/
ENV/
env.bak/
venv.bak/

# Cython debug symbols
cython_debug/
```

### Configuração blacklist

Estratégia que ignora (não faz tracking) todos os arquivos, e depois seletivamente vai adicionando os arquivos de interesse para serem trackeados:

```git
# Ignore everything:
*

# then we Whitelist (allow) anything that is a directory:
!*/

# and allow the the file types below (keep track):
!*.py
!*.png
!*.ipynb
!*.jpg
!*.jpeg
!*.gif
!*.md
!*.html

# dont track inside this folders:
.ipynb_checkpoints
*/.ipynb_checkpoints
*/__pycache__
```


### Projetos java

```git
HELP.md
target/
!.mvn/wrapper/maven-wrapper.jar
!**/src/main/**/target/
!**/src/test/**/target/

### STS ###
.apt_generated
.classpath
.factorypath
.project
.settings
.springBeans
.sts4-cache

### IntelliJ IDEA ###
.idea
*.iws
*.iml
*.ipr

### NetBeans ###
/nbproject/private/
/nbbuild/
/dist/
/nbdist/
/.nb-gradle/
build/
!**/src/main/**/build/
!**/src/test/**/build/

# Compiled class file
*.class

# Log file
*.log

# Package Files
*.jar
*.war
*.nar
*.ear
*.zip
*.tar.gz
*.rar

# virtual machine crash logs
hs_err_pid*

```

**Ver mais configurações de `.gitignore` para outros projetos:**
- https://github.com/fscheidt/gitignore

---
