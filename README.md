# 📚 It Docs Platform – Backend API

## 🧾 Loyihaning maqsadi
Ushbu Loyha foydalanuvchilarga IT yonalishidagi hujjatlar bilan tanishish, ularni oqish va kament qoldirish imkonini beradi. Barcha dokumentatsiyalar faqat **admin** tomonidan yuklanadi.

---

## ⚙️ Funksional talablar

### 👤 Foydalanuvchi (User)
- Royxatdan otishi kerak (Sign up)
- Login orqali tizimga kirishi kerak
- Profilidagi ma'lumotlarni (ism, email, parol) yangilay oladi
- Tizimga kirgach:
  - Barcha dokumentatsiyalar royxatini koradi
  - Har bir dokumentatsiyani ochib, oqiydi
  - Kommentariya yozadi
  - Boshqa foydalanuvchilarning kommentariyalarini koradi

### 🛠️ Admin
- Faqat bitta admin akkaunti mavjud
- Login orqali tizimga kiradi
- Quyidagi amallarni bajara oladi:
  - Yangi dokumentatsiya qoshadi
  - Dokumentatsiyani tahrir qiladi
  - Dokumentatsiyani ochiradi

---

## 🚀 Nofunksional talablar
- Tezkorlik
- Xavfsizlik (Token asosidagi autentifikatsiya)
- Kengaytiriluvchan REST API

---

## 🗃️ Databse modellari

### 1. Users
| Field      | Type     | Description                  |
|------------|----------|------------------------------|
| id         | Integer  | Unikal foydalanuvchi ID      |
| name       | String   | Foydalanuvchi ismi           |
| email      | String   | Email manzili                |
| password   | String   | Parol (hashlangan)           |
| role       | String   | "user" yoki "admin"          |
| createdAt  | Date     | Foydalanuvchi qoshilgan vaqt |

---

### 2. Documentation
| Field        | Type     | Description                              |
|--------------|----------|------------------------------------------|
| id           | Integer  | Unikal dokumentatsiya ID                 |
| title        | String   | Hujjat sarlavhasi                        |
| category     | String   | Yonalishi (Backend, Frontend, DevOps)   |
| content      | Text     | Dokumentatsiya matni                     |
| createdBy    | Integer  | Yaratgan admin foydalanuvchi IDsi        |
| createdAt    | Date     | Yaratilgan sana                          |

---

### 3. Comments
| Field           | Type     | Description                            |
|------------------|----------|---------------------------------------|
| id               | Integer  | Kommentariya ID                       |
| documentationId  | Integer  | Qaysi dokumentatsiyaga tegishli       |
| userId           | Integer  | Kommentariya egasi (foydalanuvchi ID) |
| content          | Text     | Kommentariya matni                    |
| createdAt        | Date     | Kommentariyaning yozilgan vaqti       |



## 📌 Texnologiyalar
- Node.js (Express.js)
- Databse MongoDb
- JWT autentifikatsiya
- bcrypt.js (password hashing)

---

## 🧠 Qoshimcha imkoniyatlar (keyinchalik kengaya olishi)
- Dokumentatsiyani PDF formatda yuklab olish
- Like / dislike tizimi
- Kommentariyani tahrirlash / ochirish
- Fikrlar soni boyicha sort qilish

