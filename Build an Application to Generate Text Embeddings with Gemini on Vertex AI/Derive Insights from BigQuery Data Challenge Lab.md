<h1 align="center">
🚀  Build an Application to Generate Text Embeddings with Gemini on Vertex AI
 ||        🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml

import vertexai
from vertexai.language_models import TextEmbeddingModel

def text_embedding(prompt):
    vertexai.init(project="YOUR_PROJECT_ID", location="us-central1")
    model = TextEmbeddingModel.from_pretrained("text-embedding-005")
    embeddings = model.get_embeddings([prompt])
    vector = embeddings[0].values
    print(f"Length of embedding vector: {len(vector)}")
    return vector

if __name__ == "__main__":
    sample_text = "Natural language processing enables computers to understand human language."
    print(f"Processing text: '{sample_text}'")
    text_embedding(sample_text)

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
