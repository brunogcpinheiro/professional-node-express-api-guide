<template>
  <div class="container">
    <h1>First Routes</h1>
    <small>(bootcamps)</small>
    <p>Now it's time to set basic routes. Create a file in <span class="word">~/routes/bootcamps.js</span> to define some basic functions in specifics routes.</p>
    <div v-highlight>
      <pre class="language-javascript">
        <code>
          const express = require("express");
          const router = express.Router();

          router.get("/", (req, res) => {
            res.status(200).json({ success: true, message: "List of all bootcamps" });
          });

          router.get("/:id", (req, res) => {
            res.status(200).json({
              success: true,
              message: `Show a bootcamp with id: ${req.params.id}`
            });
          });

          router.post("/", (req, res) => {
            res.status(200).json({ success: true, message: "Create a bootcamp" });
          });

          router.put("/:id", (req, res) => {
            res.status(200).json({
              success: true,
              message: `Update a bootcamp with id: ${req.params.id}`
            });
          });

          router.delete("/:id", (req, res) => {
            res.status(200).json({
              success: true,
              message: `Delete a bootcamp with id: ${req.params.id}`
            });
          });

          module.exports = router;
        </code>
      </pre>  
    </div>
    <p>And then load the routes in <span class="word">~/server.js</span> like this:</p>
    <div v-highlight>
      <pre class="language-javascript">
        <code>
          // Route files
          const bootcamps = require("./routes/bootcamps");
          
          // ...
          // const app = express();

          // Mount routes
          app.use("/api/v1/bootcamps", bootcamps);

          // const PORT = process.env.PORT || 5000;
          // ...
        </code>
      </pre>  
    </div>
    <div class="footer">
      <nuxt-link to="/getting-started">
        <Button>Back step: Getting Started</Button>
      </nuxt-link>
      <nuxt-link to="/abstract-routes-and-add-controllers">
        <Button>Next step: Abstract Routes and add Controllers</Button>
      </nuxt-link>
    </div>
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
small {
  color: #329132;
}
</style>

