# Сайт студии Rec Studio

## Как поменять ссылки и контакты
Откройте `index.html` и найдите блок **НАСТРОЙКИ** (в начале `<script>`, примерно строка 469):

- `whatsapp` — номер без «+» и пробелов: `77716828254`
- `telegram` — ник без @
- `instagram` — ник Instagram (пусто — кнопка скрыта)
- `showreel` — ID шоурила на YouTube Shorts. Из ссылки `youtube.com/shorts/AbC123xyz` берите `AbC123xyz`
- `metrika` — номер счётчика Яндекс Метрики
- `calculator: false` — спрятать калькулятор
- `subsPerMin`, `voicePerMin` — доплаты в калькуляторе

## Как добавить работу
В массиве `WORKS` скопируйте любую строку `{seg:..., ...}` и поменяйте:
- `seg`: `ads` — реклама, `memory` — еске алу и юбилей, `edu` — уроки и подкасты, `motion` — моушн и ИИ
- `v: true` — вертикальное видео, `false` — горизонтальное
- `yt` — ID видео на YouTube (тогда сайт откроет YouTube), или положите файлы в папку `media`:
  `loop` — превью 5–6 секунд без звука, `poster` — картинка, `file` — полный ролик (до 10–15 МБ)
- `t` — название на трёх языках, `d` — короткое описание

## Ссылки на разделы (для OLX и Instagram)
- `…/#reklama` — реклама и креативы
- `…/#eske-alu` — еске алу и юбилей
- `…/#obuchenie` — уроки и подкасты
- `…/#motion` — моушн и ИИ

## Публикация на GitHub Pages
1. github.com → New repository → имя, например `rec-studio` → Public → Create.
2. «uploading an existing file» → перетащите все файлы и папку `media` → Commit changes.
3. Settings → Pages → Branch: `main`, папка `/ (root)` → Save.
4. Через 1–2 минуты сайт будет по адресу `https://ВАШ-НИК.github.io/rec-studio/`.
5. Чтобы превью ссылки в WhatsApp показывало картинку, замените в `index.html`
   `content="og.jpg"` на полный адрес: `content="https://ВАШ-НИК.github.io/rec-studio/og.jpg"`.
