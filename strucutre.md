logmaks.github.io/
├─ _config.yml
├─ index.html                  # ваша главная (можно оставить как есть)
├─ about/
│  └─ index.html               # страница About (EN по умолчанию, RU переключается)
└─ assets/
   ├─ avatar.jpg               # (по желанию) аватар для About
   ├─ cv_en.pdf                # (по желанию) CV EN
   └─ cv_ru.pdf                # (по желанию) CV RU



///


Коротко: нет 🙂

_layouts/post.html — положи в корень репозитория в папку _layouts/

posts/index.html — в папку posts/

Сами посты — в _posts/ (файлы вида YYYY-MM-DD-title.md с layout: post)

Итоговая структура:

/
├─ _config.yml
├─ _layouts/
│  └─ post.html
├─ _posts/
│  └─ 2025-09-26-my-post.md
├─ posts/
│  └─ index.html
└─ about/
   └─ index.html
