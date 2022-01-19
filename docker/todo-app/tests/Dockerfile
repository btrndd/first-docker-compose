FROM mjgargani/puppeteer:trybe1.0
WORKDIR /todo-app/tests
ADD node_modules.tar.gz ./
COPY ["./package.json", "./package-lock.json", "./jest.config.js", "./"]
RUN ["npm", "install"]
ENTRYPOINT [ "npm" ]
RUN ["mkdir", "/e2e"]
COPY ./e2e ./e2e
CMD [ "test" ]