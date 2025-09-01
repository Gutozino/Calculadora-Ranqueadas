# 🏆 Calculadora de Nível do Herói

Este projeto é um exercício de lógica em **JavaScript**, que calcula o **saldo de vitórias** de um herói em batalhas e classifica o seu **nível** de acordo com o desempenho.

---

## 📌 Descrição

O programa recebe a quantidade de **vitórias** e **derrotas** de um herói.
Com base no **saldo de vitórias (vitórias - derrotas)**, ele retorna o nível do herói em uma das seguintes classificações:

* **Ferro**: saldo menor que 10
* **Bronze**: entre 11 e 20
* **Prata**: entre 21 e 50
* **Ouro**: entre 51 e 80
* **Diamante**: entre 81 e 90
* **Lendário**: entre 91 e 100
* **Imortal**: acima de 100

---

## 🧩 Código

```javascript
function calcularNivel(vitorias, derrotas) {
    let saldoVitorias = vitorias - derrotas;
    let nivel = "";

    if (saldoVitorias < 10) {
        nivel = "Ferro";
    } else if (saldoVitorias >= 11 && saldoVitorias <= 20) {
        nivel = "Bronze";
    } else if (saldoVitorias >= 21 && saldoVitorias <= 50) {
        nivel = "Prata";
    } else if (saldoVitorias >= 51 && saldoVitorias <= 80) {
        nivel = "Ouro";
    } else if (saldoVitorias >= 81 && saldoVitorias <= 90) {
        nivel = "Diamante";
    } else if (saldoVitorias >= 91 && saldoVitorias <= 100) {
        nivel = "Lendário";
    } else {
        nivel = "Imortal";
    }

    return { saldoVitorias, nivel };
}

let resultado = calcularNivel(85, 20);
console.log("O Herói tem saldo de " + resultado.saldoVitorias + " está no nível de " + resultado.nivel);
```

---

## 🚀 Como Executar

1. Copie o código para um arquivo `index.js`
2. Execute no terminal com:

   ```bash
   node index.js
   ```
3. O resultado será exibido no console.

---

## 🎮 Exemplo de Saída

Para `vitórias = 85` e `derrotas = 20`:

```
O Herói tem saldo de 65 está no nível de Ouro
```
