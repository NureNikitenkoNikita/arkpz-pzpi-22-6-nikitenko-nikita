# 🌍 IoT Disaster Monitoring System (**GeoGuard Pro**)

## 📌 Опис
Це сучасна система моніторингу природних катастроф, що використовує IoT-сенсори та зовнішні API (USGS, EONET) для збору, обробки та візуалізації даних. 
Система дозволяє стежити за:
- **Сейсмічною активністю** (землетруси)
- **Рівнем води** (повені)
- **Вулканічною активністю**
- **Пожежами**

## 🏗️ Архітектура
```
+------------+      +------------+      +------------+
|   IoT     | ---> |   Backend  | ---> |  Frontend  |
| Sensors   |      | (API, DB)  |      |  (UI/UX)   |
+------------+      +------------+      +------------+
```

## 🖥️ Технології
- **IoT:** Сенсори для збору даних
- **Backend:** JavaScript, PostgreSQL
- **Frontend:** JavaScript, Leaflet.js (карти), Chart.js (графіки)
- **API:** USGS, EONET

## 📡 IoT Сенсори
### 🏔️ Сенсори сейсмічної активності
- Вимірюють коливання земної поверхні
- Дані передаються через **USGS API**

### 🌊 Сенсори рівня води
- Моніторинг рівня води у річках та озерах
- Використовується для передбачення паводків

### 🌋 Сенсори вулканічної активності та пожеж
- Відстежують активність вулканів і пожеж
- Дані отримуються через **EONET API**

## 🖥️ Backend
### 🔌 API для збору даних
- Отримує дані від сенсорів та зовнішніх джерел
- Фільтрація за **періодом (3 дні, тиждень, місяць)** та **типом події**

### 🧠 Система прогнозування
- Аналізує отримані дані
- Визначає **критичні події** (наприклад, землетруси > 4.0 балів)

### 🔔 Система сповіщень
- Автоматично надсилає **попередження** користувачам
- Використовує **пульсуючі сповіщення** у UI

## 🎨 Frontend
### 🗺️ Інтерфейс моніторингу
- Відображає карту з **маркерами подій**
- Додає **індикатори сейсмічної активності, рівня води, вулканів та пожеж**

### ⚙️ Налаштування сповіщень
- Користувач може встановити **порогові значення**
- Налаштування зберігаються у **локальному сховищі**

### 📊 Аналітична панель
- **Графіки та статистика** за вибраний період
- Використовує **стовпчасті діаграми** з різними кольорами

### 🚨 Критичні події
- Відображає **найнебезпечніші події** окремим блоком
- Включає детальну інформацію (магнітуда, місце, час)

### 🌎 Інформація про мережу
- Відображає **IP-адресу** та **геолокацію користувача**
- Показує **найближчу подію та відстань** до неї

## 📌 Автор
- **[Nikitenko Nikita]** — IoT та Backend

## 📜 Ліцензія
MIT License © 2025

