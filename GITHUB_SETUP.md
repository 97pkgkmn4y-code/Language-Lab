# GitHub: инструкция (Windows PowerShell)

1. Распакуй архив так, чтобы `Language-Lab-Complete/00_START_HERE.md` был в корне vault. Obsidian → **Open folder as vault**.
2. GitHub → **New repository** → имя `Language-Lab` → **Private**, без автосоздания README (он уже есть).
3. Открой PowerShell в папке vault и выполни:

```powershell
git init
git branch -M main
git add .
git status --short
git commit -m "Initialize bilingual language lab"
git remote add origin https://github.com/USERNAME/Language-Lab.git
git push -u origin main
```

Подставь свой `USERNAME`. Перед `git add` проверь `.gitignore` и отсутствие приватных/платных материалов. Не вставляй токены и пароли в чат.

### Повседневная работа
```powershell
git pull --rebase
git add .
git commit -m "Log language session YYYY-MM-DD"
git push
```

Если нечего коммитить, `git commit` сообщит об этом — это нормально. На втором устройстве сначала `git clone`, затем `git pull` перед изменениями. Не редактируй один файл одновременно на двух устройствах.

### Источники ChatGPT Project
В проекте ChatGPT добавь `00_START_HERE.md`, `06_Protocols/Working_With_ChatGPT.md`, два реестра ошибок и последние занятия как файлы-источники. При изменениях **обновляй** эти вложения: GitHub URL сам по себе не гарантирует автоматическую синхронизацию Project Sources. Если репозиторий приватный, ссылка без авторизованного подключения не даёт доступ к его содержимому.

Официальное руководство Obsidian Git: https://obsidian.md/help/sync-notes
