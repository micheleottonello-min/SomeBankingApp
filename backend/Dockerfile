FROM python

WORKDIR /app

RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/micheleottonello-min/SomeBankingApp temp_repo \
    && mv temp_repo/backend/* . \
    && rm -rf temp_repo

RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 8000

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]