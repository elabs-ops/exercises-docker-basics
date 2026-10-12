FROM ubuntu:24.04
WORKDIR /usr/src/app
COPY --chmod=755 . .
RUN apt-get update && apt-get install -y curl
RUN curl -fsSL https://deb.nodesource.com/setup_16.x | bash -&& apt-get install -y nodejs
RUN npm install && npm run build && npm install -g serve
EXPOSE 5001
CMD ["serve", "-s", "-l", "5001", "build"]
