---
up: [[5.1 Sistema de numeración binaria]]
---
# Convertir Binario a Decimal

Para convertir una dirección IPv4 binaria a su equivalente decimal punteada, divida la dirección IPv4 en cuatro octetos de 8 bits. A continuación, aplique el valor de posición binario al primer octeto del número binario y calcule según corresponda.

Por ejemplo, suponga que 11000000.10101000.00001011.00001010 es la dirección IPv4 binaria de un host. Para convertir la dirección binaria a decimal, comience con el primer octeto, como se muestra en la tabla. Introduzca el número binario de 8 bits en el valor de posición de la fila 1 y, después, calcule para producir el número decimal 192. Este número entra en el primer octeto de la notación decimal punteada.

Valor posicional 128 64 32 16 8 4 2 1 Número binario (11000000) 11000000 Calcular1286432168421 Añadir… 128+ 64+ 0+ 0+ 0+ 0+ 0+ 0+ 0+ 0 Resultado 192

| Valor de posición         | 128 | 64   | 32  | 16  | 8   | 4   | 2   | 1   |
| ------------------------- | --- | ---- | --- | --- | --- | --- | --- | --- |
| Número binario (11000000) | 1   | 1    | 0   | 0   | 0   | 0   | 0   | 0   |
| Cálculo                   | 128 | 64   | 32  | 16  | 8   | 4   | 2   | 1   |
| Súmelos…                | 128 | + 64 | + 0 | + 0 | + 0 | + 0 | + 0 | + 0 |
**Resultado**

**192**

A continuación, convertir el segundo octeto de 10101000 como se muestra en la tabla. El valor decimal resultante es 168 y entra en el segundo octeto.

Valor posicional 128 64 32 16 8 4 2 1 Número binario (11000000) 10101000 Calcular1286432168421 Añadirlos… 128+ 0+ 32+ 0+ 8+ 0+ 0+ 0 Resultado 168

| Valor de posición         | 128 | 64  | 32   | 16  | 8   | 4   | 2   | 1   |
| ------------------------- | --- | --- | ---- | --- | --- | --- | --- | --- |
| Número binario (10101000) | 1   | 0   | 1    | 0   | 1   | 0   | 0   | 0   |
| Cálculo                   | 128 | 64  | 32   | 16  | 8   | 4   | 2   | 1   |
| Súmelos…                | 128 | + 0 | + 32 | + 0 | + 8 | + 0 | + 0 | + 0 |
**Resultado**

**168**

Convertir el tercer octeto de 00001011 como se muestra en la tabla.

Valor posicional 128 64 32 16 8 4 2 1 Número binario (11000000) 00001011 Calcular 1286432168421 Añadirlos… 0+ 0+ 0+ 0+ 8+ 0+ 2+ 1 Resultado 11

| Valor de posición         | 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |
| ------------------------- | --- | --- | --- | --- | --- | --- | --- | --- |
| Número binario (00001011) | 0   | 0   | 0   | 0   | 1   | 0   | 1   | 1   |
| Cálculo                   | 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |
| Súmelos…                | 0   | + 0 | + 0 | + 0 | + 8 | + 0 | + 2 | + 1 |
**Resultado**

**11**

Convertir el cuarto octeto de 00001010 como se muestra en la tabla. Esto completa la dirección IP y produce **192.168.11.10**.

Valor posicional 128 64 32 16 8 4 2 1 Número binario (11000000) 00001010 Calcular 1286432168421 Añadirlos… 0+ 0+ 0+ 0+ 8+ 0+ 2+ 0 Resultado 10

| Valor de posición         | 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |
| ------------------------- | --- | --- | --- | --- | --- | --- | --- | --- |
| Número binario (00001010) | 0   | 0   | 0   | 0   | 1   | 0   | 1   | 0   |
| Cálculo                   | 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |
| Súmelos…                | 0   | + 0 | + 0 | + 0 | + 8 | + 0 | + 2 | + 0 |
**Resultado**

**10**
