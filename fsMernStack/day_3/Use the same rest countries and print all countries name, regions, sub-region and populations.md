# Use the same rest countries and print all countries name, regions, sub-region and populations

```js
let xhr = new XMLHttpRequest();

xhr.open('GET', 'https://restcountries.com/v3.1/all', true);

xhr.onload = function () {
  if (xhr.status >= 200 && xhr.status < 400) {
    var data = JSON.parse(xhr.responseText);

    data.forEach(function (country) {
      var name = country.name.common;
      var region = country.region;
      var subRegion = country.subregion;
      var population = country.population;

      console.log(`Name: ${name}, Region: ${region}, Sub-Region: ${subRegion}, Population: ${population}`);
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