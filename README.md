# Engage Digital Chatbot Template for JavaScript

Template/exmaple bot use demo for [RingCentral Engage Digital chatbot js](https://github.com/ringcentral/engage-digital-chatbot-js).

## YouTube video

See the following video for a quick overview of building a chatbot with this template.

[https://youtu.be/HDDGUFIzNxQ](https://youtu.be/HDDGUFIzNxQ)

## Quick start

Let's start a simple chatbot server.

```bash
# install dependecies
npm i

# start proxy server, this will make your local bot server can be accessed by RingCentral service
npm run ngrok

# will show
Forwarding                    https://xxxx.ap.ngrok.io -> localhost:4100
# Remember the https://xxxx.ap.ngrok.io, we will use it later
```

Follow [steps to prepare email source and webhook for chatbot](https://github.com/ringcentral/engage-digital-chatbot-js/blob/master/docs/prepare-email-source-and-webhook.md) to prepare the email source and webhook.

```bash
# create env file
cp .env.sample .env
# then edit .env, set proper setting according to the tip in .env

# run local dev server
npm start

```

### Test bot

- Send a email to your predefined email source address, then bot will auto reply with `This is a auto reply by bot`.
- Edit `src/server/index.js` to set your own reply logic.

## Build

```bash
npm run build
```

## Run production code

```bash
npx ringcentral-engage-chatbot dist/server/index.js
```

## Build and deploy to AWS Lambda

[https://github.com/ringcentral/engage-digital-chatbot-js/blob/master/docs/deploy-to-lambda.md](https://github.com/ringcentral/engage-digital-chatbot-js/blob/master/docs/deploy-to-lambda.md)

## License

MIT
