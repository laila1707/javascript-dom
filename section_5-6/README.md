# Section 5

### HTML
```html
    <p>klik button di bawah untuk menuju ke repository javascript DOM github Laila</p>
    <button>
        <a id="button">Repository JavaScript</a>
    </button>
    <button>
        <a id="button2" href="https://github.com/laila1707/javascript-dom">Repository Laila tentang JavaScript DOM</a>
    </button>
```

### Script js
```js
    <script>
        //setAttribute() 
        let buttonJSDOM = document.querySelector('#button');
        if (buttonJSDOM) {
            buttonJSDOM.setAttribute('href', 'https://github.com/laila1707/javascript-dom');
        }

        //removeAttribute()
        let button2 = document.querySelector('#button2');
        if (button2){
            button2.removeAttribute('href');
        }
    </script>
```

# Section 6

### HTML
```html
    <h1 id="cek" class="cek"> Contoh getComputedStyle()</h1
```

### Script js
```js
    <script>
        //getComputedStyle
        let cek = document.querySelector('.cek');
        let style = getComputedStyle(cek);

        console.log('color:', style.color);

        //className property
        let p = document.querySelector('#cek');
        console.log(p.className);
    </script>
```