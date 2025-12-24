<img width="1174" height="916" alt="453742335-5a57dd6e-83d4-449f-88ec-1f813a450a69" src="https://github.com/user-attachments/assets/11ca2677-dccd-4dbf-a1a0-9d1048520d47" />
# 🔐 Problem logging in Wrong username or password Do you have caps lock on?

**Quick solution for n8n login problems** - Reset user management without losing workflows or credentials when facing authentication issues in self-hosted n8n instances.


## 📌 Problem Symptoms
When trying to login to your n8n self-hosted instance, you suddenly get:
- ❌ "Problem logging in. Wrong username or password. Do you have caps lock on?"
- ❌ Unable to sign in to n8n
- ❌ Authentication failed
- ❌ Login page keeps rejecting credentials
- ❐ Credentials work yesterday but not today

## 🚀 Quick Fix Solution

### Step 1: Stop n8n Service
```bash
# For systemd users
sudo systemctl stop n8n

# For PM2 users
pm2 stop n8n

# For Docker users
docker stop n8n-container

### Step 2: Reset User Management Run the Below Mentioned Command

n8n user-management:reset

### Step 3: Restart n8n


# For systemd
sudo systemctl start n8n

# For PM2
pm2 start n8n

# For Docker
docker start n8n-container


### Step 4: Create New User
Open n8n in browser (usually http://localhost:5678)

Complete setup form:
Enter your email
Create new password
Add your name
Click "Submit"


## 📌 Check n8n official Documentation 
-(https://docs.n8n.io/hosting/cli-commands/?_gl=1*11901yk*_gcl_au*MTMxNjY2MTg1OC4xNzY2NDM4Mzk1*_ga*MTgxNTI3NTY5My4xNzU2ODUwMzg3*_ga_0SC4FF2FH9*czE3NjY1OTc2MTUkbzE2JGcxJHQxNzY2NTk4ODMyJGo0NCRsMCRoMA..#user-management)
##
