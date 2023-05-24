---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home

---

<button class="btn js-toggle-dark-mode">Thème sombre</button>

<script>
const toggleDarkMode = document.querySelector('.js-toggle-dark-mode');

jtd.addEvent(toggleDarkMode, 'click', function(){
  if (jtd.getTheme() === 'dark') {
    jtd.setTheme('light');
    toggleDarkMode.textContent = 'Thème sombre';
  } else {
    jtd.setTheme('dark');
    toggleDarkMode.textContent = 'Thème clair';
  }
});
</script>