# Flowise Agents — Blog Creation & Customer Support

Simple repo containing two Flowise assets you can import/use:

- **`blog creation Agents.json`** → a Flowise *Agent Flow* that:
  1) generates a blog outline,
  2) writes the blog post,
  3) creates a LinkedIn promo post,
  4) produces a final summary/report.

- **`customerSupportAgent Chatflow.json`** → a small prompt recipe (text-based) you can reuse to build a customer support chatflow. *(It’s not a full Flowise JSON export—just the prompt steps.)*

---

## Quick Start (Docker)

1. **Run Flowise** (if not running already):
   ```bash
   docker run -d --name flowise -p 3000:3000      -v ~/.flowise:/root/.flowise      flowiseai/flowise:latest
   ```

2. **Open Flowise UI**: http://localhost:3000

3. **Import the Agent Flow**:
   - Go to **Agent Flows** → **Import** → select `blog creation Agents.json`.
   - After import, open the graph and check the **LLM node model** (change to your provider/model if needed).

4. **Use the Customer Support prompt**:
   - Open `customerSupportAgent Chatflow.json` (it’s plain text with system/user instructions).
   - Copy/paste its steps into a new **Chatflow** or **Agent Flow** inside Flowise, and wire it as you like.

> **Note on models**: The blog agent uses a generic “groqChat/openai/gpt-oss-20b” config in the JSON. Replace it with a model you have (e.g., **Ollama** `qwen2.5:3b-instruct`, `mistral:7b-instruct`, etc.), or any hosted provider key you own.

---

## Repo Structure

```
flowise-agents/
├─ blog creation Agents.json
├─ customerSupportAgent Chatflow.json
└─ README.md
```

---

## Tips

- **Faster local models** (Ollama): try `phi3:mini`, `qwen2.5:3b-instruct`, or `mistral:7b-instruct` for speed.
- **Video in README** (YouTube thumbnail link):
  ```md
  [![Demo Video](https://img.youtube.com/vi/VIDEO_ID/0.jpg)](https://www.youtube.com/watch?v=VIDEO_ID)
  ```
  Or add a local GIF: place `docs/demo.gif` and reference `![Demo](docs/demo.gif)`.

---

## GitHub — Push this folder

```bash
cd path/to/flowise-agents
git init
git add .
git commit -m "Add Flowise agents and README"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

> If the remote repo already has an initial commit (e.g., created with a README), first do:
> ```bash
> git pull origin main --allow-unrelated-histories
> git push -u origin main
> ```

---

## License

Add the license you prefer (MIT/Apache-2.0). If unsure, MIT is a friendly default.
