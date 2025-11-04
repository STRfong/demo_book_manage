# Django 專案啟動說明

## 環境需求
- Python 3.10.5

## 安裝步驟

### 1. Clone 專案
```bash
git clone <repository-url>
cd my_djangp_app（上課用）
```

### 2. 建立並啟動虛擬環境
```bash
# 建立虛擬環境
python -m venv venv

# 啟動虛擬環境
# macOS/Linux:
source venv/bin/activate

# Windows:
venv\Scripts\activate
```

### 3. 安裝相依套件
```bash
pip install -r requirements.txt
```

### 4. 設定環境變數
建立 `.env` 檔案：
```bash
DATABASE_URL=postgresql://username:password@localhost:5432/database_name
```
（開發環境使用 SQLite，可以暫時不設定）

### 5. 執行資料庫遷移
```bash
python manage.py migrate
```

### 6. 建立超級使用者（選用）
```bash
python manage.py createsuperuser
```

### 7. 啟動開發伺服器
```bash
python manage.py runserver
```

專案將在 http://127.0.0.1:8000/ 運行
