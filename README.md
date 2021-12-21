# cpython
OTUS Python Developer Professional course

Набор патчей для добавления нового функционала к интерпретатору Python 2.7.18

### inc.patch

Добавляет в интерпретатор операции инкремента `++` и декремента `--`

### until.patch 

Добавляет в интерпретатор цикл until

```python
until num == 0:
   print(num)
   num -= 1
```
### new_opcode.patch 

Добавляет в интерпретатор новый опкод LOAD_OTUS, который включает в себя два существующих опкода LOAD_FAST и LOAD_CONST
Замена этих двух опкодов на LOAD_OTUS происходит когда встречается следующий паттерн:


```bytecode
LOAD_FAST                0
LOAD_CONST               n
```
