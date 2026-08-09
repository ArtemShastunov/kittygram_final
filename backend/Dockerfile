FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt && \
    pip install --no-cache-dir gunicorn==21.2.0

COPY . .

ENV PATH="/usr/local/bin:$PATH"

CMD ["python", "-m", "gunicorn", "--bind", "0.0.0.0:8000", "kittygram_backend.wsgi"]