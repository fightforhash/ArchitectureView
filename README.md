# 10-module

## Codespaces Setup with localhost.run for Ollama

### Ollama Server Setup (External Access Required)
1. Open New Terminal
2. `curl -fsSL https://ollama.com/install.sh | sh`
3. **Important**: `OLLAMA_HOST=0.0.0.0 ollama serve` (Allow external port access)

### Tunneling Ollama with localhost.run
1. Open New Terminal  
2. `ssh -R 80:localhost:11434 ssh.localhost.run`
3. Copy the generated public URL (e.g., https://xxxxxxx.lhr.life)
4. **Important**: Update the axios URL in `backend/routes/record.mjs` line 87:
   - Change `url: "https://b95f83fc3cacca.lhr.life/api/generate"` 
   - To `url: "https://your-localhost-run-url.lhr.life/api/generate"`

### Download LLM Model
1. Open New Terminal
2. `ollama pull gemma2:2b`

### Update axiosResponse URL in record.mjs
- In `backend/routes/record.mjs`, change the axios request URL to the URL provided by localhost.run
- Example: `url: "https://your-localhost-run-url.lhr.life/api/generate"`

## Run Ollama Server (Local Development)
1. Open New Terminal
2. `curl -fsSL https://ollama.com/install.sh | sh`
3. `ollama serve`

## Pull and Chat with a Large Language Model (LLM) Conversational AI
1. Open New Terminal
2. `ollama pull gemma2:2b`

## Run ExpressJS Backend Server
1. Open New Terminal
2. `cd backend`
3. `npm install`
4. `node server.mjs`
5. Make the Port Visibility `Public`
6. Copy the forwarded address ExpressJS

## Run React.js Frontend Server
1. Copy your ExpressJS Forwarded Address
2. Create `.env` file and paste it after `REACT_APP_BACKEND_URL=` following: (use `example.env` as reference)
2. Open New Terminal
3. `cd client`
4. `npm install`
5. `npm start`

## Environment Variables Configuration
⚠️ **Important**: URLs change depending on Codespaces instance!
- Update `REACT_APP_BACKEND_URL` in both `client/example.env` and `frontend/.env` files with your current Codespaces backend URL for proper functionality.
- Example: `REACT_APP_BACKEND_URL=https://your-codespace-name-5050.app.github.dev`
