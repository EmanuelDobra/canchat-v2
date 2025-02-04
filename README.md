# Windows Dev Setup
1. Install Ubuntu from store (or whatever OS you prefer)
2. From Ubuntu terminal:
  a. Install node v22.13.1
  b. Install nvm (optional)
  c. Install miniconda3
4. Follow official docs: https://docs.openwebui.com/getting-started/advanced-topics/development
  a. Clone the Repository
  b. Frontend Setup
  c. Backend Setup
5. 
  a. Run frontend `npm run dev`
  b. Run backend `cd backend` & `sh dev.sh`

# Windows Docker-Desktop Setup
1. Install Docker Desktop
2. Make sure your `run.sh` file has the correct env setup `--env-file ./.env \`  
3. Use bash to exec `run.sh`
4. Run the newly created docker container 
