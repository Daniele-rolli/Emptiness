<!DOCTYPE html>
<!-- svelte-ignore a11y-missing-attribute -->
<html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<!-- stylesheets -->
<link rel="stylesheet" href="../src/css/navbar.css">
<link rel="stylesheet" href="../src/css/index.css">
<link rel="stylesheet" href="../src/css/mode.css">

<!-- Load an icon library -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.1/css/all.min.css" integrity="sha512-MV7K8+y+gLIBoVD59lQIYicR65iaqukzvf/nwasF0nqhPay5w/9lJmVM2hMDcnK1OnMGCdVK+iQrJ7lzPJQd1w==" crossorigin="anonymous" referrerpolicy="no-referrer" />

<!-- webpage -->
  <body>

<div class="navbar">
  <a class="active" href="/" text-align: center><i class="fa fa-fw fa-home"></i></a> 
  <a href="/"><i class="fas fa-arrow-left"></i></a> 
  <a href="1"><i class="fa-solid fa-arrow-right"></i></a>
  <a href="chapters"><i class="fa-solid fa-indent"></i></a> 
  <button id="toggle-dark-mode">
    <i class="fa-solid fa-moon"></i>
    </button>
</div>

  </body>
  <script>
    const toggleButton = document.getElementById('toggle-dark-mode');
    toggleButton.addEventListener('click', () => {
      document.body.classList.toggle('dark-mode');
    });
  </script>
   <script>
    const body = document.querySelector('body');
    const prefersDark = window.matchMedia('(prefers-color-scheme: dark)');
    
    function handleDarkPreferences(event) {
      if (event.matches) {
        body.classList.add('dark-mode');
      } else {
        body.classList.remove('dark-mode');
      }
    }
    
    prefersDark.addListener(handleDarkPreferences);
    handleDarkPreferences(prefersDark);
  </script>
  
</html>