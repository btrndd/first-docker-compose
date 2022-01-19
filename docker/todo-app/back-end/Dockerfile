FROM node:14-alpine3.12
WORKDIR /todo-app/back-end
ADD node_modules.tar.gz ./
COPY ["./package.json", "./package-lock.json", "./.gitignore", "./"]
RUN ["npm", "install"]
EXPOSE 3001
RUN ["mkdir", "/src"]
COPY ./src ./src
ENTRYPOINT [ "npm" ]
CMD [ "start" ]