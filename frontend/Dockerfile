FROM node

WORKDIR /app

RUN git clone https://github.com/micheleottonello-min/SomeBankingApp temp_repo \
    && mv temp_repo/frontend/* . \
    && rm -rf temp_repo

RUN npm install

EXPOSE 80

CMD ["npm", "start", "--", "--host", "0.0.0.0", "--port", "80"]