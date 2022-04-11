FROM nodejs:latest
ENV NODE_ENV="develop"

# Copy app's source code to the /app directory
COPY app.js /app

# The application's directory will be the working directory
WORKDIR /app

# Install Node.js dependencies defined in '/app/packages.json'
RUN npm install express --save

ENV PORT 3000
EXPOSE 3000

# Start the application
CMD ["npm", "start"]