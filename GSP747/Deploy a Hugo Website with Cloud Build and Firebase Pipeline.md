<h1 align="center">
🚀  Deploy a Hugo Website with Cloud Build and Firebase Pipeline
 || GSP747       🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1 Create firebase.json.

```lookml

{
  "hosting": {
    "public": "public",
    "ignore": [
      "firebase.json",
      "**/.*",
      "**/node_modules/**"
    ],
    "cleanUrls": true,
    "rewrites": [
      { "source": "**", "destination": "/index.html" }
    ]
  }
}

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
