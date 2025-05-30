markdown
Challenges Faced During CI/CD Pipeline Setup

1. Deleted Workflow Logs
- Accidentally deleted old workflow logs.
- Only the last four successful runs are available for reference.

2. Missing Test Script
- The initial test job failed due to the absence of a test script in `package.json`.
- *Solution:* Added the following script:
  json
  "test": "mocha test//*.test.js"
  

3. Runner Setup Confusion
- Faced uncertainty whether to run the runner setup command using Git Bash or CMD on Windows.
- *Solution:* Git Bash worked fine for registering the runner.

4. Self-Hosted Runner Registration Error
- Encountered trust/permission errors during registration.
- *Solution:* Re-registered the runner with admin privileges and skipped service mode when needed.

5. PM2 Deployment Path Issue
- Workflow was configured for `index.js`, but my entry point was `src/server.js`.
- *Solution:* Adjusted deployment scripts and PM2 configuration accordingly.

