# Setup

### Setup the .env file
* Copy .env.example to server/.env
* Replace the API keys with your own test API keys

### Start the node server.

In one terminal window:
```
cd covid-response-donations/server
npm install
npm start
```

### Forward webhooks (optional)

In another terminal:
```
cd covid-response-donations/server
stripe listen --forward-to localhost:4242/webhook
```
Copy the webhook signing secret to server/.env

### Testing
* Go to localhost:4242 to access the app
* Submit a donation
* Can test with any of the Stripe test cards
* If forwarding webhooks, check server/donations.log file to see a list of email addresses with successful donations.
