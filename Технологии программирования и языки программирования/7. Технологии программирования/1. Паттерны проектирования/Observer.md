[[Паттерны проектирования]]

Это поведенческий паттерн, созданный для того, чтобы:
- Одним - предоставлять возможность подписки на событие (которых больше!)
- Другим - предоставлять возможность отправлять подписчикам сведения о совершаемых изменениях 
![[Pasted image 20250424135656.png]]

Квадратики - классы. Пустые полоски - тут пишутся атрибуты класса. Ниже - методы класса. То есть в классе Subject имеется три метода (например setState() - устанавливает состояние объекта). Пунктиры от классов - это то, как обновляется то или иное состояние (то есть при вызове метода setState() вызывается метод update() для всех читателей).

Пример с телеграммом: уведомление прилетело от тг, что пришло новое сообщение, потом мы зашли в тк и запросили показать сообщение, далее мы его читаем.

### Достоинства и недостатки
Достоинства
	 1. Можно уведомить всех пользователей о событии (уведомление) - механизм отправленных сообщений.
	 2. Издатели не зависят от конкретных классов подписчиков и наоборот.

Недостатки
	 1. Сообщение об изменённом состоянии может не дойти до пользователя, происходит в случайном порядке (Пример: 9:00 МСК в тг самый нагруженный период)

### Примере