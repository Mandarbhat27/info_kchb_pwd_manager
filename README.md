# info_kchb_pwd_manager

> An open-source, self-hostable enterprise internal account & password management system built with Django and PostgreSQL.

[English](#english) | [繁體中文](#繁體中文-1)

---

## English

### Overview

`info_kchb_pwd_manager` is a lightweight, self-hosted system that helps organizations centrally manage employee accounts, credentials and per-system access. It targets a common pain point for small and medium-sized teams: keeping track of which employee has which account on which internal system, and reliably revoking that access when staff leave.

### Features

- **Employee management** — track basic employee data, department, job title, hire/leave dates and active status.
- **System management** — maintain the name, URL and notes for each internal system.
- **Credential mapping** — manage the account/password relationship between employees and systems, with support for access revocation.
- **Safeguards** — enforce that each employee can hold only one account per system.
- **Import/Export** — bulk import and export data via Excel (pandas / openpyxl).

### Tech stack

- **Backend:** Django 6.0.4
- **Database:** PostgreSQL (psycopg2)
- **Data processing:** pandas, openpyxl
- **Language:** Python 3.x

### Data models

| Model | Description |
|---|---|
| `Employee` | Employee records |
| `SystemApp` | System records |
| `Account` | Credential mapping (core) |

### Installation

```bash
# 1. Create a virtual environment
python -m venv venv
venv\Scripts\activate

# 2. Install dependencies
pip install -r requirements.txt
```

### Environment Configuration

Copy `.env.example` to `.env` and update the values:

```env
DB_NAME=postgres
DB_USER=postgres
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=5432
```

Environment variables:

- DB_NAME: PostgreSQL database name
- DB_USER: PostgreSQL username
- DB_PASSWORD: PostgreSQL password
- DB_HOST: Database host
- DB_PORT: Database port

```bash
# 3. Run database migrations
python manage.py migrate

# 4. Start the development server
python manage.py runserver
```


### Notes

- Database connection settings are in `config/settings.py`.
- Do not commit `.env` or any files containing secrets to version control.

### License

This project is released under the [MIT License](LICENSE).

---

## 繁體中文

企業內部帳號密碼管理系統，用於統一管理員工在各系統的帳號與密碼配置。

### 功能說明

- **員工管理**：記錄員工基本資料、所屬單位、職稱、到職/離職日期及在職狀態
- **系統管理**：維護公司內部各系統的名稱、網址與說明
- **帳密配置**：管理員工與各系統之間的帳號密碼對應關係，支援權限取消功能
- **防呆機制**：確保每位員工在同一系統只能擁有一組帳號

### 技術架構

- **後端框架**：Django 6.0.4
- **資料庫**：PostgreSQL（psycopg2）
- **資料處理**：pandas、openpyxl（支援 Excel 匯入匯出）
- **Python**：3.x

### 資料模型

| 模型 | 說明 |
|---|---|
| `Employee` | 員工資料表 |
| `SystemApp` | 系統資料表 |
| `Account` | 帳密配置表（核心） |

### 安裝與執行

1. 建立虛擬環境
```bash
python -m venv venv
venv\Scripts\activate
```

2. 安裝套件
```bash
pip install -r requirements.txt
```

3. 執行資料庫遷移
```bash
python manage.py migrate
```

4. 啟動開發伺服器
```bash
python manage.py runserver
```

### 注意事項

- 資料庫連線設定請參考 `config/settings.py`
- 請勿將 `.env` 或含有機密資訊的設定檔上傳至版本控制
