<template>
  <div class="container">
    <h1>Getting Started</h1>
    <p>To initiate a project we need to create a <span class="word">~/package.json</span> file to manage all our dependencies in the project. For this, type the command:</p>
    <div v-highlight>
      <pre class="language-javascript">
        <code>npm init</code>
      </pre>  
    </div>
    <p>After anwser the questions, the <span class="word">package.json</span> was generated, and we can write scripts and see all the dependencies of the project.</p>  
    <p>Next step is install express and dotenv.</p>
    <div v-highlight>
      <pre class="language-javascript">
        <code>npm install express dotenv</code>
      </pre>  
    </div>
    <p>Create a file called <span class="word">~/server.js</span> in the root folder. This file is the application entry point and it's responsible to create our server and run the app. We need to load the environment variables too. In the end we'll have something like this:</p>
    <div v-highlight>
      <pre class="language-javascript">
        <code>
          const express = require("express");
          const dotenv = require("dotenv");
          const app = express();

          // Load env vars
          dotenv.config({ path: "./config/config.env" });

          //Body Parser
          app.use(express.json());

          const PORT = process.env.PORT || 5000;

          app.listen(
            PORT,
            console.log(
              `Server running in ${process.env.NODE_ENV} mode on port ${PORT}`
            )
          );
        </code>
      </pre>  
    </div>
    <p>And the environment variables goes in <span class="word">~/config/config.env</span></p>
    <div v-highlight>
      <pre class="language-javascript">
        <code>
          NODE_ENV=development
          PORT=5000
        </code>
      </pre>  
    </div>
    <p>Install nodemon as a development dependency and create the following scripts in <span class="word">~/package.json</span></p>
    <div v-highlight>
      <pre class="language-javascript">
        <code>
          npm install -D nodemon
        </code>
      </pre>  
    </div>
    <div v-highlight>
      <pre class="language-javascript">
        <code>
          // ...
          "scripts": {
            "start": "NODE_ENV=production node server.js",
            "dev": "nodemon server.js"
          },
          // ...
        </code>
      </pre>  
    </div>
    <p>After, run the app:</p>
    <div v-highlight>
      <pre class="language-javascript">
        <code>
          npm run dev
        </code>
      </pre>  
    </div>
  </div>
</template>

<script>
export default {
  name: "Getting-Started"
}
</script>

<style scoped>
p {
  margin: 10px 0;
}
</style>


