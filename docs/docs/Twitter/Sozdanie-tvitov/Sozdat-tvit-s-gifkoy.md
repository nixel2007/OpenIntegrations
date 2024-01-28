---
sidebar_position: 3
---

# Создать твит с гифкой
Создает твит с гифкой


Функция СоздатьТвитГифки(Знач Текст, Знач МассивГифок, Знач Параметры = "") Экспорт

  | Параметр | Тип | Назначение |
  |-|-|-|
  | Текст | Строка | Текст твита |
  | МассивГифок | Массив из Строка, Двоичные данные | Массив двоичных данных или путей к гифкам |
  | Параметры | Структура (необяз.) | Параметры / перезапись стандартных параметров (см. [Получение необходимых данных](../)) |
  
  Вовзращаемое значение: Соответствие - сериализованный JSON ответа от Telegram


```bsl title="Пример кода"
	
	МассивКартинок = Новый Массив;
	МассивКартинок.Добавить("C:\1.gif");
	МассивКартинок.Добавить("C:\2.gif");

	Ответ = OPI_Twitter.СоздатьТвитГифки("Гифки", МассивКартинок, Параметры);
	Ответ = OPI_Инструменты.JSONСтрокой(Ответ);
	
```

![Результат](img/2.png)

```json title="Результат"

{
 "data": {
  "text": "Природа https://t.co/VWkWU11111",
  "id": "1746086669499924991",
  "edit_history_tweet_ids": [
   "1746086669499924991"
  ]
 }
}

```