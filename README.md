# 🔔 GitHub Webhook Listener with MongoDB & Live UI

This project captures GitHub events (Push, Pull Request, Merge) via webhooks and displays them in a clean, auto-refreshing UI.

## 📁 Repositories

- **action-repo**: A sample repository where GitHub activity (push, PR, merge) triggers webhooks.
- **webhook-repo**: A Flask server that:
  - Receives webhook events
  - Stores them in MongoDB
  - Serves a UI that polls and displays updates every 15 seconds

## ⚙️ Features

- GitHub Webhook integration
- MongoDB event storage
- Timestamp formatting (UTC)
- Clean frontend UI that auto-refreshes
- Handles Push, Pull Request, and Merge events

## 🧪 How It Works

1. A webhook is set up on `action-repo` pointing to the `/webhook` endpoint of `webhook-repo`.
2. The Flask server receives GitHub event payloads and saves them in MongoDB.
3. The UI (served at `/`) fetches and displays the latest events every 15 seconds.

## 🖥️ Technologies Used

- Python Flask
- MongoDB / MongoDB Atlas
- GitHub Webhooks
- HTML, CSS, JavaScript (Vanilla)

## 🛠️ Setup Instructions (webhook-repo)

1. Clone the `webhook-repo`:
   ```bash
   git clone https://github.com/your-username/webhook-repo.git
   cd webhook-repo
