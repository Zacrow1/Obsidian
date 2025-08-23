# Barra de progreso
#tecnologia #javascript #tipo+ejemplo #tema+interfaz-de-usuario #estado+completo
---
Bar: <progress max=100 value=0></progress> 0%

<script>
  var progressBar = document.querySelector('progress');
  var value = 0;
  setInterval(function() {
    value += 10;
    progressBar.value = value;
  }, 1000);
</script>
---
