# Travel MCP만 독립 HTTP 컨테이너로 실행한다. Policy MCP는 Backend의 stdio 자식 프로세스다.
FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt /tmp/requirements.txt
RUN python -m pip install --no-cache-dir -r /tmp/requirements.txt

COPY mcp_server /app/mcp_server

CMD ["python", "mcp_server/travel_server.py"]
