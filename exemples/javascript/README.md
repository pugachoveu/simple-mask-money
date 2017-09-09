# SimpleMaskMoney Exemple Javascript
First, install it.
```shell
  npm i simple-mask-money --save
```
Then, use it as follows:
```html
  <body>
    <!-- 
      inner html you put type text and inputmode numeric to mobile show only numbers 
     -->
    <input type="text" inputmode="numeric" placeholder="R$0,00">

    <script src="./node_modules/simple-mask-money/lib/simple-mask-money.js"></script>
    <script>
      // select the element 
      let input = document.getElementsByTagName('input')[0];
      
      // configuration
      SimpleMaskMoney.args = {
        preffix: '',
        suffix: '',
        fixed: true,
        fractionDigits: 2,
        decimalSeparator: ',',
        thousandsSeparator: '.'
      };
      
      // Call the method on event listeners of your input
      input.oninput = () => {
        input.value = SimpleMaskMoney.format(input.value);
      };
    </script>
  </body>
```