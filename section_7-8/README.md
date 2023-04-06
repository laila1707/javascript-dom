# Section 7

### HTML
```html
    <button id="btn_1">Button 1</button>
	<button id="btn_2">Button 2</button>
```

### Script js
```js
    <script>
		// Menambahkan event listener untuk Button 1
		const btn_1 = document.getElementById("btn_1");
		btn_1.addEventListener("click", function() {
			alert("Anda menekan Button 1!");
		});

		// Menambahkan event listener untuk Button 2
		const btn_2 = document.getElementById("btn_2");
		btn_2.addEventListener("click", function() {
			alert("Anda menekan Button 2!");
		});
	</script>
```

# Section 7_2

### HTML
```html
    <button id="btnKeys">Klik button dengan tombol Alt, Shift, Ctrl di keyboard Anda</button>
    <p id="messageKeys"></p>
```

### Script js
```js
    <script>
        let btnKeys = document.querySelector('#btnKeys');

        btnKeys.addEventListener('click', (e) => {
            let keys = [];

            if (e.shiftKey) keys.push('shift');
            if (e.ctrlKey) keys.push('ctrl');
            if (e.altKey) keys.push('alt');
            if (e.metaKey) keys.push('meta');

            let msg = document.querySelector('#messageKeys');
            msg.textContent = `Keys: ${keys.join('+')}`;
        });
    </script>
```

# Section 8

### HTML
```html
    <p>Pilih Jenis Kelamin Anda:</p>
    <div>
        <input type="radio" name="gender" value="Perempuan" id="p">
        <label for="pe">Perempuan</label>
    </div>
    <div>
        <input type="radio" name="gender" value="Laki-laki" id="l">
        <label for="laki">Laki-laki</label>
    </div>

    <p>
        <button id="btn">Tunjukan hasil</button>
    </p>

    <p id="output"></p>
```

### Script js
```js
    <script>
        const btn = document.querySelector('#btn');        
        const radioButtons = document.querySelectorAll('input[name="gender"]');
        btn.addEventListener("click", () => {
            let selectedGender;
            for (const radioButton of radioButtons) {
                if (radioButton.checked) {
                    selectedGender = radioButton.value;
                    break;
                }
            }
            // show the output:
            output.innerText = selectedGender ? `Anda berjenis kelamin ${selectedGender}` : `Anda belum memilih jenis kelamin`;
        });
    </script>
```

# Section 8_2

### HTML
```html
    <p>Pilih makanan favoritmu:</p>
    <label for="c1"> <input type="checkbox" name="food" value="sate" id="c1">Sate</label>
    <label for="c2"><input type="checkbox" name="food" value="bakso" id="c2">Bakso</label>
    <label for="c3"><input type="checkbox" name="food" value="mie" id="c3">Mie</label>
    <p>
        <button id="btn">Pilih makanan mu</button>
    </p>
```

### Script js
```js
    <script>
        const btn = document.querySelector('#btn');
        btn.addEventListener('click', (event) => {
            let checkboxes = document.querySelectorAll('input[name="food"]:checked');
            let values = [];
            checkboxes.forEach((checkbox) => {
                values.push(checkbox.value);
            });
            alert(values);
        });    
    </script>
```