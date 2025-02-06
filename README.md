# Windows Dev Setup
1. Install Ubuntu from store (or whatever OS you prefer)
2. From Ubuntu terminal:
  - Install node v22.13.1
  - Install nvm (optional)
  - Install miniconda3
3. Azure SSH Setup
  - In bash: `ssh-keygen -t rsa -b 4096 -C "your_email@ecn.forces.gc.ca"`
  - In bash: `cat /home/username/.ssh/id_rsa.pub` (or use xclip)
  - Copy your key
  - Navigate to `https://dev.azure.com.mcas.ms/CMP-CPM/_usersSettings/keys` and add your newly generated key
  - Clone the Repository `git clone git@ssh.dev.azure.com:v3/CMP-CPM/AI%20Prototypes/canchat-v2`
4. Follow official docs steps 2 & 3 at https://docs.openwebui.com/getting-started/advanced-topics/development 
  - Frontend Setup
  - Backend Setup
5. Setup app (every time after initial setup)
  - Run frontend `npm run dev`
  - Run backend `cd backend` & `sh dev.sh`
  - Connect at http://localhost:5173/

## CORS Error
Navigate to `canchat-v2/backend/open_webui/main.py` and change cors origins to the following:
```python
origins = [
    "http://localhost:5173"
]

app.add_middleware(
    CORSMiddleware,
    # allow_origins=CORS_ALLOW_ORIGIN,
    allow_origins=origins,
    allow_credentials=True,
    allow_methods=["*"],
    allow_headers=["*"],
)
```

Then you should be able to remove the code, and it should still work. 

## Pull Code Fromm SSC
```bash
git remote show origin
git remote add origin git@ssh.dev.azure.com:v3/CMP-CPM/AI%20Prototypes/canchat-v2
git remote rm origin
git remote add origin git@github.com:EmanuelDobra/canchat-v2.git
```

# Windows Docker-Desktop Setup
1. Install Docker Desktop
2. Make sure your `run.sh` file has the correct env setup `--env-file ./.env \`  
3. Use bash to exec `run.sh`
4. Run the newly created docker container 
