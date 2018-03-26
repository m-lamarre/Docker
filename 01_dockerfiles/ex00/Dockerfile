# opening VIM with an alpine container

FROM alpine:latest

RUN apk update
RUN apk upgrade
RUN apk add vim

CMD [ "vim" ]

# docker build -t vimimage:1.0 .
