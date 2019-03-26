# vue-personal-site

=================

## Steps to follow

1. Instalar Node and npm
2. Instalar vue cli dependency
3. Instalar visual studio code
4. Instalar extensiones en Chrome y en editor.

```
vue create vue-personal-site
cd vue-personal-site
npm run serve
```

## Crear componentes principales

- Crear ficheros que son **páginas** dentro del directorio: ```/pages```
- Crear ficheros que son **plantillas** dentro del directorio: ```/layouts```
- Crear ficheros que son **componentes** dentro del directorio: ```/components```

Pages:

1. Home

Layouts:

1. Main

Componentes:

1. Menú
2. Header
3. Footer

### Ejemplo de componente / layout / page

IMPORTANTE:

- Debe de haber una etiqueta ```<template></template>``` para el HTML.
- Debe de haber una etiqueta ```<script></script>``` para el Javascript.
- Debe de haber una etiqueta ```<style></style>``` para el CSS.

```
<template>
  <main>
    <h2>Main</h2>
  </main>
</template>

<script>
export default {
  name: 'Main'
}
</script>

<style scoped>
  main {
    margin: 20px;
    padding: 20px;
  }
</style>
```

- Dentro de la etiqueta ```<template></template>``` lo más importante es que haya un tag contenedor que englobe todo.

- Dentro de la etiqueta ```<script></script>``` lo más importante es que haya un `export default {}` y que tenga al menos 'name' como atributo.

- Incluiremos la etiqueta ```<style></style>``` cuando necesitemos incluir estilos al componente en el que estamos. E incluiremos el atributo scoped cuando queremos que estos estilos se adhieran al componente. Si quisiéramos que fueran generales esos estilos no ponemos el atributo scoped.

## Estructura de proyecto

Hasta ahora nuestro proyecto habrá crecido un poco y tendrá esta estructura.

```
src/
  assets/
  components/
    TheFooter.vue
    TheHeader.vue
    TheMenu.vue
  layouts/
    Main.vue
  pages/
    Home.vue
  App.vue
```

### Componentes:

  TheFooter.vue

  ```
    <template>
      <footer>
        <h2>Footer</h2>
      </footer>
    </template>

    <script>
    export default {
      name: 'Footer',
    }
    </script>

    <style scoped>
      footer {
        background-color: #000000;
        color: #ffffff;
        margin: 0;
        padding: 40px;
      }
    </style>

  ```

  TheHeader.vue

  ```
    <template>
      <header>
        <h1>Hello, I am Cristina</h1>
        <p>Frontend Developer</p>
      </header>
    </template>

    <script>
    export default {
      name: 'Header'
    }
    </script>

    <style scoped>
      header {
        border: 10px solid #ffffff;
        padding: 20px;
        margin: 20px;
        text-align: left;
      }
    </style>
  ```

  TheMenu.vue

  ```
    <template>
      <nav>
        <div>M</div>
        <div>X</div>
      </nav>
    </template>

    <script>
    export default {
      name: 'TheMenu'
    }
    </script>

    <style scoped>
      nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin: 20px;
      }
    </style>
  ```

### Plantillas:

  Main.vue

    ```
      <template>
        <main>
          <h2>Main</h2>
        </main>
      </template>

      <script>
      export default {
        name: 'Main'
      }
      </script>

      <style scoped>
        main {
          margin: 20px;
          padding: 20px;
        }
      </style>
    ```

### Páginas:

  Home.vue

    ```
    <template>
      <div>
        <the-menu />
        <the-header />
        <Main />
        <the-footer />
      </div>
    </template>

    <script>
    import TheMenu from '@/components/TheMenu.vue'
    import TheHeader from '@/components/TheHeader.vue'
    import TheFooter from '@/components/TheFooter.vue'
    import Main from '@/layouts/Main.vue'

    export default {
      name: 'Home',
      components: {
        TheMenu,
        TheHeader,
        TheFooter,
        Main
      }
    }
    </script>
    ```

### App:

  App.vue

  ```
    <template>
      <div id="app">
        <Home />
      </div>
    </template>

    <script>
    import Home from './pages/Home.vue'

    export default {
      name: 'app',
      components: {
        Home
      }
    }
    </script>

    <style>
    body {
      font-family: 'Avenir', Helvetica, Arial, sans-serif;
      background-color: #fd5e60;
      color: #ffffff;
      margin: 0;
    }
    </style>
  ```

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```
