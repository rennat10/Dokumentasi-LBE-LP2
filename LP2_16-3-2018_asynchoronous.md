# Review LBE

## Callback, Promise/Bluebird, Async

Javascript mempunyai kemampuan asynchronous, yaitu kemampuan mengeksekusi program tanpa harus menunggu program lainnya selesai

Beberapa fungsi yang dapat digunakan untuk implementasi dari kemampuan asyncrhonous yaitu, **callback**, **promise/bluebird**, dan juga **async**
NB: *sebaiknya jangan gunakan callback*

### Promise/Bluebird

Contoh fungsi penggunaan *Promise/Bluebird* dalam program adalah seperti berikut:

const Bluebird = require('bluebird')
```
function tambah(data){
    return new Bluebird((resolve, reject) => {
        setTimeout(function(){
            resolve(data + data)
        }, 1000);
    })
}
```
fungsi setTimeout berguna untuk mensimulasikan waktu berjalan setelah 1000 ms sebelum pemanggilan terjadi, sebelum itu, kita mereturn nilai Bluebird

### Async

Contoh fungsi penggunaan *Async* dalam program adalah seperti berikut:
```
const myFunc = async () => {
    const x = await tambah(10);
    const y = await kali(2);

    console.log(x + ' ' + y);
};
```
Saya masih belum terlalu paham dengan penggunaan fungsi async dikarenakan node js yang saya gunakan belum tersedia fungsi async
