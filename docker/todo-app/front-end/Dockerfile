FROM node:14-alpine3.12
WORKDIR /todo-app/front-end
ADD node_modules.tar.gz ./
COPY ["./package.json", "./package-lock.json", "./.env", "./.gitignore", "./README.md", "./"]
RUN ["npm", "install"]
EXPOSE 3000
RUN ["mkdir", "/src"]
COPY ./src ./src
RUN mkdir /public
COPY ./public ./public
ENTRYPOINT [ "npm" ]
CMD [ "start" ]