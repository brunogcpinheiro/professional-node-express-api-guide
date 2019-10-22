<template>
  <div class="container">
    <h1>Hello, developer!</h1>
    <br />
    <p>Welcome! This guide is intended to show you the walkthrough 
      for creating a professional API using NodeJS and Express.</p>
    <h4>This guide is based on <a href="">Brad Traversy</a> course on Udemy! Buy the course: <a href="https://www.udemy.com/course/nodejs-api-masterclass" target="_blank">here</a></h4>
    <p>For this, we will use the following <strong>frameworks/tools:</strong></p>
    <div class="technologies">
      <div class="techs">
        <img src="~assets/nodejs.png" alt="NodeJS">
        <p>NodeJS</p>
      </div>
      <div class="techs">
        <img src="~assets/npm.png" alt="NPM">
        <p>Node Package Manager</p>
      </div>
      <div class="techs">
        <img src="~assets/express.png" alt="Express">
        <p>Express</p>
      </div>
      <div class="techs">
        <img src="~assets/mongodb.png" alt="MongoDB">
        <p>MongoDB</p>
      </div>
      <div class="techs">
        <img src="~assets/mongoose.png" alt="Mongoose">
        <p>Mongoose</p>
      </div>
      <div class="techs">
        <img src="~assets/postman.png" alt="Postman">
        <p>Postman</p>
      </div>
    </div>
    <p>We be able to create an API that manage Bootcamps, Reviews, Courses, Users, Authentication, Security and much more!</p>  
    <h2>I'm Bruno Carpinelli and you can find me <a href="#">here</a></h2>
    <br />
    <br />
    <nuxt-link to="/getting-started">
      <Button>Next step: Getting started</Button>
    </nuxt-link>
  </div>
</template>

<script>
import Button from "@/components/Button.vue";

export default {
  components: {
    Button
  }
}
</script>


<style scoped>
p {
  line-height: 2;
  margin: 10px 0;
}

a {
  color: #4a26ec;
}

.technologies {
  width: 100%;
  margin-top: 20px;
  display: flex;
  align-items: center;
  justify-content: space-around;
}

.techs {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.techs img {
  height: 70px;
}

.techs p {
  font-weight: bold;
  fonts-size: 1.1rem;
}
</style>
