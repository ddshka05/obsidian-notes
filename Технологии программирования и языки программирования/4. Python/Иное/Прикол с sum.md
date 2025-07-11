У функции `sum()` есть начальное значение, которое по умолчанию равно нулю, его можно менять через именованный аргумент `start`. Это помогает лишиться проблем при суммировании различных типов данных, например
```python
from datetime import timedelta

deltas = [timedelta(hours=1),
          timedelta(hours=2),
          timedelta(hours=3)]

print(sum(deltas, start=timedelta()))    # 6:00:00
```
