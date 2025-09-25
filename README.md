# 👋 Фёдор  Рожин «Fron»
![Python](https://img.shields.io/badge/python-3.11-blue?logo=python)  ![Blender](https://img.shields.io/badge/Blender-000000?logo=blender&logoColor=F5792A)  ![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white)

---

## 🧑‍💻 Обо мне  
Я — студент 2 курса факультета Радиоэлектроники и информационных технологий, УрФУ.  
С детства кодил на **Python**: алгоритмы, компьютерное зрение, мини-нейросети, веб-скрипты.  
Также занимаюсь вёрсткой и фронтендом.

📌 **Когда отвечаю:**  
- В будни — после **21:00 (МСК)**  
- В пятницу / воскресенье — с **17:00 до 20:00**, и позже  
⏰

---

## 🔍 Интересы  
- Алгоритмы и структуры данных  
- Компьютерное зрение / машинное обучение  
- Веб / фронтенд-микрозадачи  
- 3D-моделирование и анимация (Blender)

---

## 🛠 Навыки

| Направление | Поднавыки |
|-------------|------------|
| **Python** | алгоритмы, оптимизация, мини-нейросети, прототипирование |
| **Веб** | HTML / CSS, простая вёрстка |
| **Инструменты / окружение** | Git / GitHub, VS / WebStorm, облачные сервисы (Yandex.Cloud) |
| **3D / Blender** | статичные сцены, ручная анимация, физика |

---

## 📆 График «не беспокоить»

| День недели | Доступно для сообщений |
|-------------|--------------------------|
| Пн — Чт      | после 21:00               |
| Пятница      | 17:00 — 20:00 и после 21:00 |
| Воскресенье  | 17:00 — 20:00 и после 21:00 |
| Суббота      | после 21:00               |

---

## 🚀 Проекты и достижения  
- Мини-нейросеть для распознавания  
- Скрипты для обработки изображений  
- Сайт-портфолио и другие микропроекты 
```python
# compact_digit_128.py — запуск: python compact_digit_128.py
import tensorflow as tf
from tensorflow.keras import layers, models

bs=32; img=(128,128)
train = tf.keras.utils.image_dataset_from_directory("data/train", image_size=img, batch_size=bs)
val   = tf.keras.utils.image_dataset_from_directory("data/val",   image_size=img, batch_size=bs)

model = models.Sequential([
  layers.Rescaling(1./255, input_shape=(*img,3)),
  layers.Conv2D(16,3,activation='relu'), layers.MaxPool2D(),
  layers.Conv2D(32,3,activation='relu'), layers.MaxPool2D(),
  layers.Conv2D(64,3,activation='relu'),
  layers.GlobalAveragePooling2D(),
  layers.Dense(64,activation='relu'),
  layers.Dense(10,activation='softmax')
])

model.compile(optimizer='adam', loss='sparse_categorical_crossentropy', metrics=['acc'])
model.fit(train, validation_data=val, epochs=10)
model.save('digits128.h5')

```
---

## 📫 Контакты  
- **Telegram**: [@Fron_dr](https://t.me/Fron_dr)  
- **Почта**: Fedor.Rozhin@urfu.me  

---

![GitHub stats](https://github-readme-stats.vercel.app/api?username=Fron4ick&show_icons=true&theme=dark)


