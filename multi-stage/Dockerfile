FROM alpine as git
RUN apk add git

FROM git as fetch
WORKDIR /repo
RUN git clone https://github.com/nagisatosanae/k8s-study-step07-web-contents.git .

FROM nginx
COPY --from=fetch /repo/index.html /usr/share/nginx/html