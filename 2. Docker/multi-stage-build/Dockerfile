FROM alpine as first 
WORKDIR /multi-stage
COPY ./abc.cpp /multi-stage
WORKDIR /multi-stage
RUN apk update && apk add g++ && g++ abc.cpp -o abc

FROM alpine as second
WORKDIR /multi-stage
RUN apk add libstdc++ 
COPY --from=first /multi-stage /multi-stage


