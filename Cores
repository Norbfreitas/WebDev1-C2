const colors = [
     'aliceblue', 'antiquewhite', 'aqua', 'aquamarine', 'azure', 'beige', 'bisque', 'black', 'blanchedalmond', 'blue',
    'blueviolet', 'brown', 'burlywood', 'cadetblue', 'chartreuse', 'chocolate', 'coral', 'cornflowerblue', 'cornsilk',
    'crimson', 'cyan', 'darkblue', 'darkcyan', 'darkgoldenrod', 'darkgray', 'darkgreen', 'darkgrey', 'darkkhaki',
    'darkmagenta', 'darkolivegreen', 'darkorange', 'darkorchid', 'darkred', 'darksalmon', 'darkseagreen', 'darkslateblue',
    'darkslategray', 'darkslategrey', 'darkturquoise', 'darkviolet', 'deeppink', 'deepskyblue', 'dimgray', 'dimgrey',
    'dodgerblue', 'firebrick', 'floralwhite', 'forestgreen', 'fuchsia', 'gainsboro', 'ghostwhite', 'gold', 'goldenrod',
    'gray', 'green', 'greenyellow', 'grey', 'honeydew', 'hotpink', 'indianred', 'indigo', 'ivory', 'khaki', 'lavender',
    'lavenderblush', 'lawngreen', 'lemonchiffon', 'lightblue', 'lightcoral', 'lightcyan', 'lightgoldenrodyellow',
    'lightgray', 'lightgreen', 'lightgrey', 'lightpink', 'lightsalmon', 'lightseagreen', 'lightskyblue', 'lightslategray',
    'lightslategrey', 'lightsteelblue', 'lightyellow', 'lime', 'limegreen', 'linen', 'magenta', 'maroon', 'mediumaquamarine',
    'mediumblue', 'mediumorchid', 'mediumpurple', 'mediumseagreen', 'mediumslateblue', 'mediumspringgreen',
    'mediumturquoise', 'mediumvioletred', 'midnightblue', 'mintcream', 'mistyrose', 'moccasin', 'navajowhite', 'navy',
    'oldlace', 'olive', 'olivedrab', 'orange', 'orangered', 'orchid', 'palegoldenrod', 'palegreen', 'paleturquoise',
    'palevioletred', 'papayawhip', 'peachpuff', 'peru', 'pink', 'plum', 'powderblue', 'purple', 'red', 'rosybrown',
    'royalblue', 'saddlebrown', 'salmon', 'sandybrown', 'seagreen', 'seashell', 'sienna', 'silver', 'skyblue',
    'slateblue', 'slategray', 'snow', 'springgreen', 'steelblue', 'tan', 'teal', 'thistle', 'tomato',
    'turquoise', 'violet', 'wheat', 'white', 'whitesmoke', 'yellow', 'yellowgreen'

  ];
  
  const selectedColors = [];
  const maxAttempts = 3;
  let randomColor;
  let attempts = 0;
  
  function pegarCorAleatoria() {
    return colors[Math.floor(Math.random() * colors.length)];
  }
  
  function createColorPalette() {
    const colorPalette = document.getElementById('color-palette');
    for (let i = 0; i < 10; i++) {
      const color = pegarCorAleatoria();
      selectedColors.push(color);
      const colorBox = document.createElement('div');
      colorBox.classList.add('color-box');
      colorBox.style.backgroundColor = color;
      colorBox.addEventListener('click', function() {
        document.getElementById('color-guess').value = color;
      });
      colorPalette.appendChild(colorBox);
    }
    randomColor = selectedColors[Math.floor(Math.random() * selectedColors.length)];
  }
  
  function checkGuess() {
    const guessInput = document.getElementById('color-guess');
    const resultDisplay = document.getElementById('resultado');
  
    if (!guessInput || !resultDisplay) {
      console.error("Element not found!");
      return;
    }
  
    const guess = guessInput.value.toLowerCase();
    if (guess === randomColor) {
      document.body.style.backgroundColor = randomColor;
      resultDisplay.textContent = 'BOA! Você descobriu a cor!';
    } else {
      attempts++;
      if (attempts === maxAttempts) {
        resultDisplay.textContent = `Desculpe, você perdeu! A cor era ${randomColor}.`;
      } else {
        resultDisplay.textContent = `Tente novamente! ${maxAttempts - attempts} tentativa(s) restante(s).`;
      }
    }
  }  
  createColorPalette();
