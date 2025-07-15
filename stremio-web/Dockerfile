###########################################################
# Building stage
###########################################################
FROM node:18 as build

RUN apt-get update && apt-get install -y git python3 make g++
RUN git clone https://github.com/Stremio/stremio-web.git /app

WORKDIR /app

RUN npm install
RUN npm run build

###########################################################
# Running stage
###########################################################
FROM nginx:alpine
COPY --from=build /app/build /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
