# Решатель квадратных уравнений

Модуль `quadratic_equation` вычисляет корни квадратного уровнения.

# Как использовать

Функция вычисления корней квадратного уровнения вызываеться из модуля `quadratic_equation` командой:

```python
from quadratic_equation import get_roots
```

Функция `get_roots(a, b, c)` вычисляет дискриминант по формулу `discriminant = b²-4ac` и возвращает корни квадратного уровнения `root1`, `root2` в зависимостри от дискриминанта.

```python
def get_roots(a, b, c):
    discriminant = b ** 2 - 4 * a * c
    if discriminant >= 0:
        root1 = (-b - sqrt(discriminant)) / (2 * a)
        root2 = (-b + sqrt(discriminant)) / (2 * a)
    else:
        return None, None
    if discriminant == 0:
        return root1, None
    else:
        return root1, root2
```

Если `discriminant` , больше или равен 0, то вычисляеться оба корня `root1`, `root2` и переходит к следующему условию, иначе вычисление корней не производится и функция возвращает `None`.

```python
if discriminant >= 0:
    root1 = (-b - sqrt(discriminant)) / (2 * a)
    root2 = (-b + sqrt(discriminant)) / (2 * a)
else:
```

Если `discriminant` равен нулю то функция возвращает один корень `root1`, иначе функция возвращает оба корня `root1` и `root2`

```python
if discriminant == 0:
    return root1, None
else:
    return root1, root2
```

# Как запустить

Скрипт требует для своей работы установленного интерпретатора Python версии 3.5

Запуск на Linux:

```bash
python tests.py # может понадобиться вызов python3 вместо python, зависит от настроек операционной системы
```

Запуск на Windows происходит аналогично.

# Цели проекта

Код создан в учебных целях. В рамках учебного курса по веб-разработке ― [DEVMAN.org](https://devman.org)
