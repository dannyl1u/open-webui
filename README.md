# MacBook Setup Guide for Open-WebUI

## The Mission Begins

**"The funny guys are invading, we must set up OPEN WEBUI to restore world domination!"**

## Prerequisites
Before setting up Open-WebUI, ensure the following are installed on your MacBook:

1. **Homebrew** (Package Manager)
   ```sh
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
   After installation, restart the terminal and run:
   ```sh
   brew --version
   ```
   to verify the installation.

2. **Node.js & npm**
   ```sh
   brew install node
   ```
   Verify installation:
   ```sh
   node -v
   npm -v
   ```

3. **Conda (Miniconda or Anaconda)**
   ```sh
   brew install --cask miniconda
   ```
   After installation, restart the terminal and run:
   ```sh
   conda --version
   ```

## Cloning the Repository

```sh
git clone --branch doggo --single-branch https://github.com/dannyl1u/open-webui.git
cd open-webui
```

## Frontend Setup

1. Create a `.env` file:
   ```sh
   cp -RPp .env.example .env
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

3. Start the frontend server:
   ```sh
   npm run dev
   ```
   The frontend will be available at: [http://localhost:5173](http://localhost:5173).

## Backend Setup

1. Navigate to the backend folder:
   ```sh
   cd backend
   ```

2. Create a Conda environment:
   ```sh
   conda create --name open-webui python=3.11
   conda activate open-webui
   ```

3. Install dependencies:
   ```sh
   pip install -r requirements.txt -U
   ```

4. Start the backend server:
   ```sh
   sh dev.sh
   ```

With Open-WebUI now operational, the resistance is armed and ready. The battle for world domination has begun. Good luck! 🚀

