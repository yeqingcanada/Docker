FROM node:14.16.0-alpine3.13
RUN addgroup app && adduser -S -G app app
USER app
WORKDIR /app
RUN mkdir data
COPY package*.json .
RUN npm install
COPY . . 
ENV API_URL=http://api.myapp.com/
EXPOSE 3000
CMD ["npm", "start"]
# ENTRYPOINT ["npm", "start"]



# docker build -t react-app .
# docker run -it react-app sh
# docker run react-app
# docker exec -it 716 sh
# docker run -d -p 5001:3000 react-app