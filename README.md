# JavaScript Style Guide :)

## 1. Понятные имена переменных и функций
Код легче читать, когда при написании используются понятные, описательные имена функций и переменных, отражающие их смысл.

*Правильный вариан*
``` js
function toCube(num) {
    let result = num * num * num;
    return result;
}
```
*Неправильный вариант*
``` js
function wr(a) {
    let b = a * a *a;
    return b;
}
```