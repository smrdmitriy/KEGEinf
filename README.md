# КЕГЭ | Информатика

Образовательная платформа подготовки к ЕГЭ по информатике: React, TypeScript, Vite, Tailwind CSS, Supabase.

Приложение и инструкции: [kege-platform/README.md](kege-platform/README.md).

```sh
cd kege-platform
npm ci
npm run dev
```

Корневой GitHub Actions workflow проверяет и публикует приложение из подпапки `kege-platform`.

Публикация: https://smrdmitriy.github.io/KEGEinf/

При первичной загрузке через браузер исходники сохранены в `kege-source.tar.gz`. Workflow с `contents: read` распаковывает их только во время сборки. Для обычной разработки распакуйте архив в корне репозитория (`tar -xzf kege-source.tar.gz`) и закоммитьте папку `kege-platform`. При наличии `kege-platform/package.json` архив больше не используется.

Доступ к заданиям и кабинетам закрыт до настройки Supabase. Самостоятельной регистрации нет: преподаватель создаёт ученика по почте и получает случайный пароль. Настройка: миграции 001 и 002, Edge Function create-student, отключённая публичная регистрация, публичные переменные VITE_SUPABASE_URL и VITE_SUPABASE_ANON_KEY.
