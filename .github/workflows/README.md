# GitHub Workflows

## Auto Version Bump Workflow

This workflow automatically bumps the version in `package.json` every 10 minutes and creates a pull request.

### Troubleshooting the "remote rejected" Error

If you're seeing errors like:
```
fatal error in commit_refs
[remote rejected] ... (failure)
```

This is usually caused by repository settings. Here's how to fix it:

#### Option 1: Enable Workflow Permissions (Recommended for personal repos)

1. Go to your repository on GitHub
2. Navigate to **Settings** → **Actions** → **General**
3. Scroll down to **Workflow permissions**
4. Select **"Read and write permissions"**
5. Check **"Allow GitHub Actions to create and approve pull requests"**
6. Click **Save**

#### Option 2: Use a Personal Access Token (PAT)

If you have branch protection rules or need more control:

1. Create a Personal Access Token (PAT):
   - Go to GitHub **Settings** → **Developer settings** → **Personal access tokens** → **Tokens (classic)**
   - Click **"Generate new token (classic)"**
   - Give it a name like "Version Bump Workflow"
   - Select scopes: `repo` (full control) and `workflow`
   - Generate and copy the token

2. Add the token to your repository:
   - Go to your repository **Settings** → **Secrets and variables** → **Actions**
   - Click **"New repository secret"**
   - Name: `PAT_TOKEN`
   - Value: (paste your token)
   - Click **Add secret**

3. The workflow will automatically use `PAT_TOKEN` if available, otherwise it falls back to `GITHUB_TOKEN`

#### Option 3: Disable Branch Protection Rules

If you have branch protection rules preventing direct pushes:

1. Go to **Settings** → **Branches**
2. Either:
   - Remove branch protection rules temporarily, OR
   - Add the GitHub Actions bot to the list of users who can bypass branch protection

### Testing the Workflow

You can manually trigger the workflow:
1. Go to **Actions** tab
2. Click **"Auto Version Bump"** workflow
3. Click **"Run workflow"** button
4. Select the branch and run

### Adjusting the Schedule

The workflow currently runs every 10 minutes. To change this, edit the cron schedule in `version-bump.yml`:

```yaml
schedule:
  - cron: '*/10 * * * *'  # Every 10 minutes
```

Common cron patterns:
- `*/5 * * * *` - Every 5 minutes
- `*/30 * * * *` - Every 30 minutes
- `0 * * * *` - Every hour
- `0 0 * * *` - Daily at midnight
- `0 9 * * 1` - Every Monday at 9 AM
