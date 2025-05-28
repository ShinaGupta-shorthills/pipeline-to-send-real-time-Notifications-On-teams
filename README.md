# pipeline-to-send-real-time-Notifications-On-teams
Create a GitHub Actions CI pipeline that sends real-time notifications to a Microsoft Teams channel based on the pipeline status. The notification should indicate whether the pipeline succeeded or failed.


🚀 EC2 Auto Deployment with Teams Notification
This GitHub Actions workflow automates the deployment of an Ubuntu EC2 instance on AWS, installs Nginx, and sends a real-time success or failure notification to a Microsoft Teams channel.

🔧 Key Features:
Launches a new EC2 instance using AWS CLI.

Automatically installs and starts Nginx via SSH.

Sends deployment status (✅ Pass / ❌ Fail) to Microsoft Teams using a webhook.

Uses GitHub Secrets to securely handle credentials and keys.

🛠️ Trigger:
Manually triggered via the workflow_dispatch event.

📩 Notifications:
Ensure you configure an Incoming Webhook in Teams and save it as a secret named TEAMS_WEBHOOK in your GitHub repo.

🧩 Technical Tasks:
 Create .github/workflows/ci-teams-notify.yml

 Configure Teams webhook and store as TEAMS_WEBHOOK_URL in GitHub Secrets

 Use conditional steps in GitHub Actions to detect job result

 Format JSON payload for Teams adaptive card

 Test with dummy commits to ensure both SUCCESS and FAIL messages are triggered

