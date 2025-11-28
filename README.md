

## 📊 Dataset
- MovieLens 25M
- 62,000+ movies
- 25M+ ratings
- 162,000+ users
# dowload https://grouplens.org/datasets/movielens/25m/
# Di chuyển file ml-25m.zip vào data/raw/
mv ~/Downloads/ml-25m.zip data/raw/
# Giải nén
Expand-Archive ml-25m.zip -DestinationPath . 

# Di chuyển file (nếu cần)
Move-Item ml-25m\* .

# Xóa thư mục và ZIP
Remove-Item -Recurse -Force ml-25m
Remove-Item -Force ml-25m.zip

# Windows PowerShell
python -m venv .venv

# Kích hoạt
.venv\Scripts\Activate.ps1

Cài dependencies:
pip install -r requirements.txt
Note scikit-surprise lỗi