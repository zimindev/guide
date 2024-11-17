
# Міні гайд по wget

`wget` — це потужний інструмент командного рядка для завантаження файлів з інтернету.

## 1. Завантаження одного файлу
```bash
wget [URL]
```
Приклад:
```bash
wget https://example.com/file.zip
```

## 2. Завантаження файлу з вказівкою імені
```bash
wget -O [ім'я_файлу] [URL]
```
Приклад:
```bash
wget -O newfile.zip https://example.com/file.zip
```

## 3. Завантаження файлу в фоновому режимі
```bash
wget -b [URL]
```
Це дозволяє завантажувати файли в фоновому режимі, не блокуючи термінал.

## 4. Завантаження декількох файлів
```bash
wget -i [файл_зі_списком_посилань]
```
Приклад:
```bash
wget -i links.txt
```

## 5. Завантаження файлів рекурсивно (ціла веб-сторінка або каталог)
```bash
wget -r [URL]
```
Приклад:
```bash
wget -r https://example.com/somefolder/
```

## 6. Завантаження з обмеженням швидкості
```bash
wget --limit-rate=[швидкість] [URL]
```
Приклад:
```bash
wget --limit-rate=200k https://example.com/file.zip
```

## 7. Відновлення перерваного завантаження
```bash
wget -c [URL]
```
Приклад:
```bash
wget -c https://example.com/file.zip
```

## 8. Завантаження з аутентифікацією
```bash
wget --user=[користувач] --password=[пароль] [URL]
```
Приклад:
```bash
wget --user=admin --password=secret https://example.com/file.zip
```

## 9. Завантаження з проксі
```bash
wget -e use_proxy=yes -e https_proxy=[URL проксі] [URL]
```
Приклад:
```bash
wget -e use_proxy=yes -e https_proxy=http://proxy.example.com:8080 https://example.com/file.zip
```

## 10. Використання HTTPS з перевіркою SSL
```bash
wget --secure-protocol=auto [URL]
```

Це лише базовий набір команд, `wget` має багато додаткових опцій, які можуть бути корисні в різних випадках. Виведення команд можна побачити, виконавши:
```bash
man wget
```
