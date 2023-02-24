FROM node:16.18

ENV PORT=3000
#comments in files very important
COPY . /frontend-react-js
WORKDIR /frontend-react-js
RUN npm install
EXPOSE ${PORT}
CMD ["npm", "start"] 