# Windows Dev Setup
1. Install Ubuntu from store (or whatever OS you prefer)
2. From Ubuntu terminal:
  - Install node v22.13.1
  - Install nvm (optional)
  - Install miniconda3
4. Follow official docs: https://docs.openwebui.com/getting-started/advanced-topics/development
  - Clone the Repository
  - Frontend Setup
  - Backend Setup
5. Setup app
  - Run frontend `npm run dev`
  - Run backend `cd backend` & `sh dev.sh`

# Windows Docker-Desktop Setup
1. Install Docker Desktop
2. Make sure your `run.sh` file has the correct env setup `--env-file ./.env \`  
3. Use bash to exec `run.sh`
4. Run the newly created docker container 
