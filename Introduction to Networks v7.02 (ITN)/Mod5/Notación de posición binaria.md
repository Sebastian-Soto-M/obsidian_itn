## Notación de posición binaria

Para aprender a convertir de sistema binario a decimal, es necesario entender la notación de posición. El término "notación de posición" significa que un dígito representa diferentes valores según la "posición" que el dígito ocupa en la secuencia de números. Ya conoce el sistema de numeración más común, el sistema de notación decimal (de base 10).

El sistema de notación posicional decimal funciona como se describe en la tabla.

Radix 10101010 Posición en el número 3210 Calcular (103) (102) (101) (100) Posición valor 1000100101

| Radix                | 10    | 10    | 10    | 10    |
| -------------------- | ----- | ----- | ----- | ----- |
| Posición en número   | 3     | 2     | 1     | 0     |
| Cálculo              | (103) | (102) | (101) | (100) |
| Valor de la posición | 1000  | 100   | 10    | 1     | 

Las viñetas siguientes describen cada fila de la tabla.

-   Fila 1, Radix es la base numérica. La notación decimal se basa en 10, por lo tanto, la raíz es 10.
-   Fila 2, Posición en número considera la posición del número decimal que comienza con, de derecha a izquierda, 0 (1ª posición), 1 (2ª posición), 2 (3ª posición), 3 (4ª posición). Estos números también representan el valor exponencial utilizado para calcular el valor posicional en la cuarta fila.
-   Fila 3 calcula el valor posicional tomando la raíz y elevándola por el valor exponencial de su posición en la fila 2.   
    **Nota:** n0 es = 1.
-   El valor posicional de la fila 4 representa unidades de miles, cientos, decenas y unos.

Para usar el sistema de posición, una un número dado con su valor de posición. El ejemplo en la tabla ilustra cómo se usa la notación posicional con el número decimal 1234.

Miles Cientos Decenas Unos Valor posicional 1000100101 Número decimal (1234) 1234 Calcular1 x 10002 x 1003 x 104 x 1Añadirlos... 1000+ 200+ 30+ 4 Resultado1,234

|                       | Millares | Centenas | Decenas | Unidades |
| --------------------- | -------- | -------- | ------- | -------- |
| Valor de posición     | 1000     | 100      | 10      | 1        |
| Número decimal (1234) | 1        | 2        | 3       | 4        |
| Cálculo               | 1 x 1000 | 2 x 100  | 3 x 10  | 4 x 1    |
| Add them up…          | 1000     | + 200    | + 30    | + 4      |


**Resultado**

**1,234**

En contraste, la notación posicional binaria opera como se describe en la tabla.

Radix 22222222 Posición en Número76543210Calcular (27) (26) (25) (24) (23) (22) (21) (20) Posición valor 1286432168421

| Radix                | 2    | 2    | 2    | 2    | 2    | 2    | 2    | 2    |
| -------------------- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| Posición en número   | 7    | 6    | 5    | 4    | 3    | 2    | 1    | 0    |
| Cálculo              | (27) | (26) | (25) | (24) | (23) | (22) | (21) | (20) |
| Valor de la posición | 128  | 64   | 32   | 16   | 8    | 4    | 2    | 1    |

Las viñetas siguientes describen cada fila de la tabla.

-   Fila 1, Radix es la base numérica. La notación binaria se basa en 2, por lo tanto, el radix es 2.
-   Fila 2, Posición en número considera la posición del número binario que comienza con, de derecha a izquierda, 0 (1ª posición), 1 (2ª posición), 2 (3ª posición), 3 (4ª posición). Estos números también representan el valor exponencial utilizado para calcular el valor posicional en la cuarta fila.
-   Fila 3 calcula el valor posicional tomando la raíz y elevándola por el valor exponencial de su posición en la fila 2.   
    **Nota:** n0 es = 1.
-   El valor posicional de la fila 4 representa unidades de uno, dos, cuatro, ocho, etc.

El ejemplo en la tabla ilustra cómo un número binario 11000000 corresponde al número 192. Si el número binario fuera 10101000, el número decimal correspondiente sería 168.

Valor posicional 1286432168421 Número binario (11000000) 11000000 Calcular1 x 1281 x 640 x 320 x 160 x 80 x 40 x 20 x 1 Añadir.. 128+ 64+ 0+ 0+ 0+ 0+ 0+ 0+ 0+ 0 Resultado 192

| Valor de posición         | 128     | 64     | 32     | 16     | 8     | 4     | 2     | 1     |
| ------------------------- | ------- | ------ | ------ | ------ | ----- | ----- | ----- | ----- |
| Número binario (11000000) | 1       | 1      | 0      | 0      | 0     | 0     | 0     | 0     |
| Cálculo                   | 1 x 128 | 1 x 64 | 0 x 32 | 0 x 16 | 0 x 8 | 0 x 4 | 0 x 2 | 0 x 1 |
| Añádanlos..               | 128     | + 64   | +0     | + 0    | + 0   | + 0   | + 0   | + 0   |

**Resultado**

**192**