# mohammed.Eng# مشروع نظام إدارة المهام والمشاريع (Project Management System)

هذا المشروع هو تطبيق ويب متكامل لإدارة المشاريع، المهام، الموظفين، والمالية. تم بناؤه باستخدام تقنيات حديثة لضمان السرعة والكفاءة.

---

## 🛠 التقنيات المستخدمة (Tech Stack)

| الجزء | التقنيات |
| :--- | :--- |
| **الواجهة الأمامية (Frontend)** | React, Vite, TypeScript, Tailwind CSS, Shadcn UI |
| **الخادم (Backend)** | Node.js, Express, TypeScript |
| **قاعدة البيانات (Database)** | PostgreSQL, Drizzle ORM |
| **أدوات التطوير** | tsx, ESBuild |

---

## 🚀 طريقة التشغيل (Quick Start)

### 1. المتطلبات الأساسية
تأكد من تثبيت الأدوات التالية على جهازك:
*   [Node.js](https://nodejs.org/) (إصدار 18 فما فوق).
*   [PostgreSQL](https://www.postgresql.org/) (أو قاعدة بيانات سحابية مثل [Neon.tech](https://neon.tech/)).

### 2. التثبيت (Installation)
افتح الـ Terminal في مجلد المشروع وقم بتشغيل الأمر التالي لتثبيت المكتبات:
```bash
npm install
```

### 3. إعداد قاعدة البيانات (Database Setup)
قم بإنشاء ملف باسم `.env` في المجلد الرئيسي للمشروع، وأضف رابط قاعدة البيانات الخاص بك:
```env
DATABASE_URL=postgres://user:password@localhost:5432/db_name
```

### 4. التشغيل (Running the Project)

#### لمستخدمي Windows (PowerShell):
لتشغيل الخادم وواجهة المستخدم معاً:
```powershell
$env:NODE_ENV="development"; $env:PORT=5000; npx tsx server/index.ts
```

#### لمستخدمي Linux/macOS:
```bash
NODE_ENV=development PORT=5000 npx tsx server/index.ts
```

---

## ⚠️ حل المشاكل الشائعة (Troubleshooting)

### خطأ `NODE_ENV is not recognized`
هذا الخطأ يظهر في Windows. الحل هو استخدام الأمر المدمج في PowerShell المذكور أعلاه، أو تثبيت مكتبة `cross-env`:
```bash
npm install cross-env --save-dev
```
ثم تعديل ملف `package.json` ليحتوي على `"dev": "cross-env NODE_ENV=development tsx server/index.ts"`.

### خطأ `ENOTSUP: operation not supported on socket 0.0.0.0:5000`
يحدث هذا الخطأ في بعض إصدارات Windows. لحله، قم بتعديل ملف `server/index.ts` وتغيير العنوان من `0.0.0.0` إلى `127.0.0.1` أو `localhost`.

### خطأ `SASL: SCRAM-SERVER-FIRST-MESSAGE`
هذا يعني أن كلمة مرور قاعدة البيانات غير صحيحة أو غير موجودة في ملف `.env`. تأكد من صحة رابط `DATABASE_URL`.

---

## 📂 هيكلية المشروع (Project Structure)

*   `client/`: كود الواجهة الأمامية (React).
*   `server/`: كود الخادم والـ API (Express).
*   `shared/`: المخططات المشتركة (Database Schemas).
*   `scripts/`: نصوص برمجية لاستيراد البيانات أو الصيانة.

---

## 📄 الترخيص
هذا المشروع مخصص للأغراض التعليمية والتطويرية.
