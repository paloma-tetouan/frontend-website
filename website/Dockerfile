FROM nginx:1.21.6-alpine

RUN apk --update --no-cache upgrade \
    && apk add git vim nodejs npm \
	&& rm -rf /var/lib/apt/lists/*

WORKDIR /usr/share/nginx/html

COPY nginx.conf /etc/nginx/conf.d/default.conf
COPY ./website package.json package-lock.json ./

RUN npm install
