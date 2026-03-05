Sum - LeetCode
Dado um array de números e um valor alvo (target), precisamos encontrar dois números que somados resultem nesse alvo e retornar os índices deles.
Exemplo

Entrada:
nums = [2, 7, 11, 15]  
target = 9  

Saída:
[0, 1]

Porque:
2 + 7 = 9 


omo eu pensei na solução

Ao invés de testar todos os pares possíveis (usando dois loops), eu pensei assim:
Para cada número do array, eu posso calcular quanto falta para chegar no target.
Se:

valorAtual = 7  
target = 9  

Então o número que eu preciso encontrar é:

9 - 7 = 2

Ou seja, se eu já tiver visto o número 2 antes, eu já encontrei a solução.

Para fazer essa verificação rápida, usei um HashMap.

No mapa eu guardo:
- o número como chave
- o índice como valor

Assim consigo verificar em tempo O(1) se o complemento já apareceu.
