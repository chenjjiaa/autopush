# GitHub Actions Permission Setup Guide

## Step 1: Generate Access Token
1. Navigate to:  
   `Settings → Developer Settings → Personal access tokens → Tokens (classic)`
2. Click `Generate new token (classic)`
3. Name your token (e.g., `YOUR_TOKEN`) and **copy the generated secret** (it will be hidden after you leave this page)
4. Select required permissions:
   - [x] `repo` (Full repository access)
   - [x] `workflow` (Workflow permissions)

## Step 2: Add Token to Repository Secrets
1. Go to your repository's:  
   `Settings → Secrets and variables → Actions`
2. Select the **Secrets** tab (not Variables)
3. Click `New repository secret`
4. Enter:
   - Name: `YOUR_TOKEN` (must match your workflow references)
   - Value: Paste the secret copied in Step 1

## Step 3: Enable Workflow Permissions
1. Navigate to:  
   `Settings → Actions → General`
2. Under **Workflow permissions**:
   - Select `Read and write permissions`

✅ **Verification Tip**:  
Run a test workflow to confirm the permissions are working.

---

### Troubleshooting
If encountering errors:
1. Verify token hasn't expired.
2. Confirm correct permission scopes were selected.
3. Ensure secret name matches exactly in workflows.
