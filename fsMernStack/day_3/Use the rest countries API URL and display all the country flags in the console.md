###  Use the rest countries `API URL` -> ***https://restcountries.com/v3.1/all***  and display all the country flags in the console.f
```js
let xhr = new XMLHttpRequest();

xhr.open('GET', 'https://restcountries.com/v3.1/all', true);

xhr.onload = function () {
  if (xhr.status >= 200 && xhr.status < 400) {
    var data = JSON.parse(xhr.responseText);

    data.forEach(function (country) {
      var flag = country.flags.svg;
      console.log(flag);
    });
  } else {
    console.error('Error:', xhr.status, xhr.statusText);
  }
};

xhr.onerror = function() {
  console.error('Network error');
};

xhr.send();
```
