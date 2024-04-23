# Tutorial Modul 8 - Subscriber
---
### Muhammad Yusuf Haikal
### 2206081490
### Pemrograman Lanjut A
---

## 1. How many data your publlsher program will send to the message broker in one run?
Program tersebut akan mengirimkan 5 data kepada message broker dalam satu run, berdasarkan pada bagian kode 
```_ = p.publish_event("user_created".to_owned(), UserCreatedEventMessage { user_id: "1".to_owned(), user_name: "2206081490y-Amir".to_owned() });
_ = p.publish_event("user_created".to_owned(), UserCreatedEventMessage { user_id: "2".to_owned(), user_name: "2206081490-Budi".to_owned() });
_ = p.publish_event("user_created".to_owned(), UserCreatedEventMessage { user_id: "3".to_owned(), user_name: "2206081490-Cica".to_owned() });
_ = p.publish_event("user_created".to_owned(), UserCreatedEventMessage { user_id: "4".to_owned(), user_name: "2206081490-Dira".to_owned() });
_ = p.publish_event("user_created".to_owned(), UserCreatedEventMessage { user_id: "5".to_owned(), user_name: "129500004y-Emir".to_owned() });
```
Dimana tiap line akan mengirimkan satu pesan ke queue `user_created`.

## 2. The url of: `amqp://guest:guest@localhost:5672` is the same as in the subscriber program, what does it mean?
Kedua program terhubung pada server message broker yang sama, pada kasus ini `RabbitMQ`.

Penggunaan URL yang sama pada publisher dan subscriber memungkinkan mereka untuk berkomunikasi melalui message broker RabbitMQ yang sama. Publisher mengirimkan pesan ke antrian "user_created", dan subscriber mendengarkan pada antrian yang sama untuk menerima pesan tersebut.




