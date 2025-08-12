# Calculadora-basica
Proyecto de práctica en JavaScript que incluye una calculadora básica con suma, resta, multiplicación y división.
## Objetivos

1. Implementar las cuatro operaciones aritméticas básicas: suma, resta, multiplicación y división.  
2. Crear una interfaz intuitiva con botones para números y operaciones.  
3. Aprender a manipular el DOM con JavaScript para interactuar con el usuario.

## Tecnologías utilizadas

- HTML  
- CSS  
- JavaScript

> "La práctica es el camino hacia la perfección."

[Página oficial de GitHub](https://github.com/Jhohanmelgar/Calculadora-basica)

![Ejemplo de calculadora](https://via.placeholder.com/300x150.png?text=Calculadora+B%C3%A1sica)

```html
<!-- Ejemplo de estructura HTML básica para la calculadora -->
<div class="calculadora">
  <div id="display">0</div>
  <button data-value="1">1</button>
  <button data-value="2">2</button>
  <button data-value="+">+</button>
  <button data-value="=">=</button>
</div>
<script>
  // Ejemplo de lógica JavaScript sencilla
  const display = document.getElementById('display');
  document.querySelectorAll('button').forEach(btn => {
    btn.addEventListener('click', () => {
      const val = btn.getAttribute('data-value');
      if (val === '=') {
        display.textContent = eval(display.textContent);
      } else {
        display.textContent = display.textContent === '0' ? val : display.textContent + val;
      }
    });
  });
</script>