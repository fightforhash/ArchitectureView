# 10-module

## Run Ollama Server
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
