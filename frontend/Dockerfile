FROM node:8.16 as builder

WORKDIR /usr/src/app
COPY package.json yarn.lock ./
RUN yarn install --ignore-engines
COPY . ./
RUN yarn build

FROM nginx:1.23.1-alpine
COPY --from=builder /usr/src/assets/bundles /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g" , "daemon off;" ]



