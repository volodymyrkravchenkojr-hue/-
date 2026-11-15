КАК СОБРАТЬ APK
1. Загрузите все файлы этого архива в репозиторий GitHub (включая папки www, assets, .github).
2. Actions -> Build APK -> Run workflow. Через 5-10 минут скачайте rotations-apk из раздела Artifacts.
3. Установите app-debug.apk на телефон.

ЧТОБЫ ОБНОВЛЕНИЯ СТАВИЛИСЬ ПОВЕРХ СТАРОЙ ВЕРСИИ (без удаления)
Добавьте секрет KEYSTORE_B64 в репозиторий:
Settings -> Secrets and variables -> Actions -> New repository secret.
Имя: KEYSTORE_B64. Значение: содержимое файла keystore-secret.txt (отдельный файл, не в этом архиве).
После этого все сборки подписываются одним ключом.

ЗНАЧОК
Файлы в папке assets (icon-only.png, icon-foreground.png, icon-background.png, 1024x1024)
можно заменить своими. Сборка сама сделает из них значки для Android.

ОБНОВЛЕНИЕ ПРИЛОЖЕНИЯ
Замените www/index.html и запустите Build APK ещё раз.
