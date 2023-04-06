# Section 2

### HTML
```html
    <h1 id="hai">Hai Teman-Teman</h1>
    <h3>Gimana hari ini?</h3>
    <h3>Namaku Karin</h3>
    <p>Gender:</p>
    <label for="perempuan">
        <input type="radio" name="jenisGender" value="Perempuan">Perempuan
    </label>
    <label for="laki-laki">
        <input type="radio" name="jenisGender" value="Laki-laki">Laki-laki
    </label>
    <button id="simpan">Simpan</button>
    <p id="hasil"></p>
    <button id="check">Check getElementsByTagName</button>
```

### Script js
```js
    <script>
        //getElementById()
        const hai = document.getElementById('hai');
        hai.style.fontSize = '40px';

        //getElementsByName()
        let button = document.getElementById('simpan');
        let hasil = document.getElementById('hasil');
        button.addEventListener('click', () => {
            let rates = document.getElementsByName('jenisGender');
            rates.forEach((jenisGender) => {
                if (jenisGender.checked) {
                    hasil.innerText = `Anda berjenis kelamin ${jenisGender.value}`;
                }
            });
        });

        //getElementByTagName
        let btn = document.getElementById('check');
        btn.addEventListener('click', () => {
            let coba = document.getElementsByTagName('h3');
            alert(`Berapa jumlah tag h3? ${coba.length}`);
        });
    </script>
```

# Section 3

### HTML
```html
    <div id="coba">
        <h1>Coba-coba</h1>
        <h1 class="section-3">Section 3</h1>
    </div>
    <div>
        <h2>1. Get the parent element</h2>
        <h2 class="se3">2. Get child elements</h2>
        <h2>3. Get siblings of an element</h2>
    </div>
```
### Script js
```js
    <script>
        //Get the parent element
        let parentElemen = document.querySelector('.section-3')
        parentElemen.style.color = 'yellow';

        //Get child elements
        let getChild = parentElemen.getChild;
        let edit = document.getElementById('coba');
        edit.style.color = 'green';

        //Get siblings of an element
        let pilih = document.querySelector('.se3');
        let siblings = pilih.nextElementSibling;
        siblings.style.color = 'orange';
    </script>
```

# Section 4

### HTML
```html
    <div id="appendChild"></div>
```
### Script js
```js
        <script>
        //createElement()
        let adddiv = document.createElement('div');
        adddiv.id = 'coba';
        adddiv.innerHTML = '<h1>Ini createElement()</h1>';
        document.body.appendChild(adddiv);

        //appendChild()
        function createh3(isi_h3){
            let h3 = document.createElement('h3');
            h3.textContent = isi_h3;
            return h3;
        }
        const ini_h3 = document.querySelector('#appendChild');
        ini_h3.appendChild(createh3('Ini'));
        ini_h3.appendChild(createh3('hasil dari'));
        ini_h3.appendChild(createh3('appendChild()'));

        //innerHTML
        let inner = document.createElement('ul')
        inner.innerHTML = '<li>ini contoh</li><li>innerHTML</li>';
        document.body.appendChild(inner);
    </script>
```