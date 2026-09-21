# Backend는 stdio Policy MCP를 자식 프로세스로 실행하므로, 두 MCP Server 소스를 같은
# 이미지에 포함한다. Travel MCP는 Compose 네트워크의 별도 컨테이너로 호출한다.
FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt /tmp/requirements.txt
RUN python -m pip install --no-cache-dir -r /tmp/requirements.txt

COPY backend /app/backend
COPY mcp_server /app/mcp_server

CMD ["python", "-m", "uvicorn", "backend.app.main:app", "--host", "0.0.0.0", "--port", "8000"]
