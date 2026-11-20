# Лаб 5: API систем тест — Postman ба Newman

**F.CSA313 — Программ хангамжийн чанарын баталгаа ба тест (2026)**

| | |
|---|---|
| **Оюутан** | Д.Алтанбагана |
| **Оюутны код** | B222270827 |

## Орчин

```
$ node -v
v24.21.0

$ newman -v
6.2.3
```

Newman-ийг `sudo npm install -g newman`-ээр суулгасан. Тестлэх API бол лабын `server.js` (цэвэр Node, сан хэрэггүй): `node server.js` → `http://localhost:3000`.

## Даалгавар 1: Анхны хүсэлт ба oracle

`lab05-collection.json` доторх «Д1» хавтас: `PUT /students/B231234567` (идэвхтэй, CS201 үзсэн) → `PUT /courses/CS313` (урьдач нь CS201) → `POST /registrations`. POST дээр хоёр `pm.test` oracle байгаа: статус `201` ба `result = "OK"`. URL бүр `{{baseUrl}}` collection variable (`http://localhost:3000`) ашиглана.
