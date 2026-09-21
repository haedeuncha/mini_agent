# Frontend에는 Backend API 주소만 전달하며 MCP 주소나 OpenAI 자격 증명을 넣지 않는다.
FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt /tmp/requirements.txt
RUN python -m pip install --no-cache-dir -r /tmp/requirements.txt

COPY frontend /app/frontend

CMD ["python", "-m", "streamlit", "run", "frontend/app.py", "--server.address", "0.0.0.0", "--server.port", "8501", "--server.headless", "true"]
