# Получение объекта

Для получения объекта надо сделать GET запрос к объекту ресурса

`GET https://vozovoz.ru/api/v1/[название ресурса]/[ID]`

---

```js
HTTP/1.1 200 OK
{
    "data" : [объект]
}
```

**Пример**

`GET https://vozovoz.ru/api/v1/news`

---

```js
HTTP/1.1 200 OK
{
    "data": {
        "id":    1,
        "title": "Новость 1"
        …
    }
}
```