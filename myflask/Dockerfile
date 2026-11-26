FROM python:3.12-slim

WORKDIR /app

# 의존성 먼저 설치 (캐시 활용)
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# 소스 코드는 나중에 복사
COPY . .

EXPOSE 5000
CMD ["python", "app.py"]