# Setup

### Setup the .env file
* Copy .env.example to server/.env
* Replace the API keys with your own test API keys

### Start the node server.

In one terminal window:
    npm install
    Run npm start

### Forward webhooks

In another terminal:
    stripe listen --forward-to localhost:4242/webhook

### Testing
* Go to localhost:4242 to access the app
* Submit a donation
* Can test with any of the Stripe test cards
* Check the server/donations.log file to see a list of email addresses that we need to send receipts to.