## Iniciar un proyecto ya creado

### 1. Instalar prerequisitos dependiendo el sistema operativo

#### Arch Linux

- Instalar `sudo pacman -S ruby base-devel ruby-erb`

- Instalar `gem install jekyll bundler`

- Agregar la variable al PATH en al archivo `.profile` o `.bash_profile`

```sh
export GEM_HOME="$HOME/.local/share/gem/ruby/versionDelRuby"
export GEM_PATH="$GEM_HOME"
export PATH="$GEM_HOME/bin:$PATH"
```

Aplicar la $GEM_HOME mediante el comando `source ~/.profile` o `source ~/.bash_profile` (dependiendo el archivo en donde se agrego en el paso anterior)

### 2. Clonar el repo

### 3. Dentro de la carpeta clonada ejecutar el comando `bundle install`

### 4. Iniciar servidor para continuar editando el proyecto mediante el comando `bundle exec jekyll serve`

---

## ¿Como es el formato de fecha para nombrar un archivo de post?

año-numeroDeMes-día-como-es-el-formato-de-un-post.md
