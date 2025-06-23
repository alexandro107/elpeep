# elpeep
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Mi sitio VueD básico</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Incluye Vue.js desde CDN -->
  <script src="https://unpkg.com/vue@3/dist/vue.global.prod.js"></script>
  <style>
    body {
      background: #fafafa;
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }
    #app {
      max-width: 600px;
      margin: 40px auto;
      padding: 2rem;
      background: #fff;
      box-shadow: 0 2px 8px #0001;
      border-radius: 8px;
    }
    h1 {
      color: #42b983;
    }
    button {
      background: #42b983;
      color: #fff;
      border: none;
      padding: .5rem 1rem;
      font-size: 1rem;
      border-radius: 4px;
      cursor: pointer;
    }
    button:hover {
      background: #33966a;
    }
  </style>
</head>
<body>
  <div id="app">
    <h1>{{ titulo }}</h1>
    <p>¡Bienvenido a tu primer sitio con VueD (Vue 3 + HTML)!</p>
    <p>Has hecho clic <b>{{ contador }}</b> veces.</p>
    <button @click="contador++">Haz clic aquí</button>
  </div>
  <script>
    const { createApp } = Vue;
    createApp({
      data() {
        return {
          titulo: 'Sitio VueD de ejemplo',
          contador: 0
        }
      }
    }).mount('#app');
  </script>
</body>
</html>
