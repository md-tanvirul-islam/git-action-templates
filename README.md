# GitHub Actions Deployment Guide  

## **How These Workflows Work**  

These GitHub Actions workflows automate deployment when you push code to specific branches.  

### **Basic Flow**  
1. **Trigger**: Runs on push to `main`, `master` branches  
2. **Steps**:  
   - Checks out your code  
   - Installs dependencies (Node.js, PHP, etc.)  
   - Builds assets (if needed)  
   - Securely transfers files to your server via SSH  
   - Runs post-deployment commands (database updates, cache clearing, service restarts)  

### **What You Need to Do**  
1. **Set up secrets** in your GitHub repo settings:  
   - `SSH_PRIVATE_KEY` (Your server's SSH key)  
   - `HOST` (Server IP/hostname)  
   - `USER` (SSH username)  
   - `PROJECT_DIRECTORY` (Remote path like `/var/www/your-app`)  

2. **Push to the right branch** to trigger deployment  

3. **Monitor progress** in the GitHub Actions tab  

The workflow handles everything after you push - no manual deployment needed!  