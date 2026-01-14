Antes de llevar a cabo el proceso de instalación, puedes echarle un vistazo a como se vería tu web estática con Jekyll y WhySoSimple mediante este link: [https://whysosimple-jekylltemplate.vercel.app/](https://whysosimple-jekylltemplate.vercel.app/)

## 1. Instalar jekyll

Visita la página [https://jekyllrb.com/docs/installation/](https://jekyllrb.com/docs/installation/) para llevar a cabo una instalación adecuada dependiendo tu sistema operativo.

### Inicio rapido de instalación en Arch Linux

Instalar **`sudo pacman -S ruby base-devel ruby-erb`**

Instalar **`gem install jekyll bundler`**

Agregar la variable al PATH en al archivo `.profile` o `.bash_profile`

```sh
export GEM_HOME="$HOME/.local/share/gem/ruby/versionDelRuby"
export GEM_PATH="$GEM_HOME"
export PATH="$GEM_HOME/bin:$PATH"
```

Aplicar la `$GEM_HOME` en la terminal mediante el comando **`source ~/.profile`** o **`source ~/.bash_profile`** (dependiendo el archivo en donde agregaste la variable al PATH)

## 2. Clona este repo en tu sistema :)

![How to clone this repo WhySoSimple](assets/repoclonewhysosimple.png)

## 3. Instalar las bundler gems

Dentro de la carpeta de tu proyecto (o dentro de la carpeta de este repo clonada en tu sistema) ejecuta el comando `bundle install` en la terminal.

## 4. Iniciar servidor local web

Para iniciar el servidor local web usa el comando **`bundle exec jekyll serve`** en la terminal y dentro de la carpeta de tu proyecto (o dentro de la carpeta de este repo clonada en tu sistema)


---

Nota: La documentación adicional y completa se encuentra en el mismo repo, solo necesitas desplegar el servidor web local cuando hayas completado los pasos anteriores. En el paso número 4 se te indica como iniciar un servidor local web con jekyll.
