## Projeto: Otimização de websites

### Instruções para rodar a aplicação

  -  Iniciar servidor HTTP

  ```bash
  $> cd /caminho/para/o/projeto
  $> python -m SimpleHTTPServer 8080
  ```

  -  Abrir o navegdor e acessar localhost:8080
  -  Fazer o download e instalar o [ngrok](https://ngrok.com/) (permite que o site seja acessado remotamente).
  -  Iniciar o ngrok.

  ``` bash
  $> cd /caminho/para/o/ngrok
  $> ./ngrok http 8080
  ```
  -  O ngrok vai fornecer uma URL pública na linha de comando, que poderá ser copiada e utilizada em qualquer navegador.

### Otimizações realizadas em index.html
  - Removido Google Analytics.
  - Removido Google WebFonts.
  - Adicionado atributo media="print" na tag link que importa print.css.
  - Foi compactado o conteúdo de style.css através do site https://cssminifier.com/ e adicionado em uma tag style dentro do arquivo index.html.
  - As imagens foram compactadas.

### Otimizações realizadas em views/js/main.js
  - Alterado o método changePizzaSizes para calcular a largura de 'randomPizzaContainer' utilizando porcentagem ao invés de pixels.
  - Excluído o método determineDx, pois não era mais utilizado.
  - Alterado a quantidade de pizzas criadas na tela de 200 para 25.
