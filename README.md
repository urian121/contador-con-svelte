# Contador con Svelte

Este es un componente de contador desarrollado con [Svelte 5](https://svelte.dev), utilizando Bootstrap 5 para el diseño y los estilos. Permite incrementar, decrementar y resetear el valor del contador con una interfaz limpia y funcional.

## Resultado final

![Contador con Svelte](https://raw.githubusercontent.com/urian121/imagenes-proyectos-github/refs/heads/master/contador-con-svelte.png)


## Características
- Incrementar el contador.
- Decrementar el contador (evitando valores negativos).
- Resetear el contador.
- Botones deshabilitados según la lógica correspondiente.
- Estilo responsivo gracias a Bootstrap 5.

## Requisitos
- [Node.js](https://nodejs.org/) (v16 o superior recomendado).
- Framework [Svelte 5](https://svelte.dev).
- [Bootstrap 5](https://getbootstrap.com/) incluido en el proyecto.

## Instalación

1. Clona el repositorio:
   ```bash
   git clone https://github.com/urian121/contador-con-svelte
   cd tu_repositorio
   ```

2. Instala las dependencias:
   ```bash
   npm install
   ```

3. Ejecuta el servidor de desarrollo:
   ```bash
   npm run dev
   ```

4. Abre tu navegador en `http://localhost:5173` para ver el proyecto.

## Código del Componente

```svelte
<script>
  let count = 0;

  const increment = () => count++;
  const decrement = () => count > 0 && count--;
  const reset = () => count = 0;
</script>

<div class="row justify-content-center mt-5">
  <div class="col-md-8 text-center">
    <h3 class="fw-bold mb-4">
      Contador: <span class="display-4">{count}</span>
    </h3>

    <div class="d-flex justify-content-center gap-2">
      <button class="btn btn-success" on:click={increment}>
        <i class="bi bi-plus-circle"></i> Aumentar
      </button>

      <button
        class="btn btn-danger"
        on:click={decrement}
        disabled={count === 0}
        aria-disabled={count === 0}
      >
        <i class="bi bi-dash-circle"></i> Disminuir
      </button>

      <button
        class="btn btn-primary"
        on:click={reset}
        disabled={count === 0}
        aria-disabled={count === 0}
      >
        <i class="bi bi-arrow-counterclockwise"></i> Resetear
      </button>
    </div>
  </div>
</div>
```



### Expresiones de Gratitud 🎁

   Comenta a otros sobre este proyecto 📢
   Invita una cerveza 🍺 o un café ☕
   Paypal iamdeveloper86@gmail.com
   Da las gracias públicamente 🤓.

## No olvides SUSCRIBIRTE 👍
