# Технічна документація API

Опис основних методів API для інтеграції QuickShare із зовнішніми додатками.

## Базова URL
`https://api.quickshare.com/v1`

## Ендпоінти

### 1. Завантаження файлу
Використовується для відправки файлу на сервер.

* **Метод:** `POST`
* **URL:** `/files/upload`
* **Тіло запиту (Body):** `multipart/form-data` (файл)

**Приклад успішної відповіді (200 OK):**
```json
{
  "status": "success",
  "file_id": "abc123xyz",
  "download_link": "[https://quickshare.com/d/abc123xyz](https://quickshare.com/d/abc123xyz)",
  "expires_at": "2025-05-20T12:00:00Z"
}
