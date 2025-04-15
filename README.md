# 📚 Dokumentatsiya Platformasi – Backend API

## 🧾 Loyihaning maqsadi
Ushbu platforma foydalanuvchilarga IT yo‘nalishidagi hujjatlar bilan tanishish, ularni o‘qish va izoh qoldirish imkonini beradi. Barcha dokumentatsiyalar faqat **admin** tomonidan yuklanadi.

---

## ⚙️ Funksional talablar

### 👤 Foydalanuvchi (User)
- Royxatdan otishi kerak (Sign up)
- Login orqali tizimga kirishi kerak
- Profilidagi ma'lumotlarni (ism, email, parol) yangilay oladi
- Tizimga kirgach:
  - Barcha dokumentatsiyalar royxatini ko‘radi
  - Har bir dokumentatsiyani ochib, oqiydi
  - Kommentariya yozadi
  - Boshqa foydalanuvchilarning kommentariyalarini ko‘radi

### 🛠️ Admin
- Faqat bitta admin akkaunti mavjud
- Login orqali tizimga kiradi
- Quyidagi amallarni bajara oladi:
  - Yangi dokumentatsiya qoshadi
  - Dokumentatsiyani tahrir qiladi
  - Dokumentatsiyani o‘chiradi

---

## 🚀 Nofunksional talablar
- Tezkorlik
- Xavfsizlik (Token asosidagi autentifikatsiya)
- Kengaytiriluvchan REST API

---

## 🗃️ Ma’lumotlar bazasi modellari

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
| category     | String   | Yo‘nalishi (Backend, Frontend, DevOps)   |
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
- Fikrlar soni bo‘yicha sort qilish

