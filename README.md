# Vastralaya Ecommerce Application

This is a Next.js-based ecommerce application template integrated with Sanity for content management, Clerk for authentication, Stripe for payments, and Sendbird for chat functionality.
Follow the steps below to set up and customize the application.

## 🔗 Preview

<img width="1471" height="797" alt="image" src="https://github.com/user-attachments/assets/d08eed94-1619-45e4-97cf-6b127b589962" />


## Getting started

To set up the Vastralaya Ecommerce Application, follow these steps carefully:

### 1. Install npm Dependencies

First, install the required npm dependencies by running the following command in your terminal depend with package you are using:

```bash
npm install
or
yarn install
or
pnpm install
```

This will download all the necessary packages listed in package.json.

## 2. Create a New Sanity Project

Set up a Sanity project to manage your ecommerce content (e.g., products or blog posts):

```bash
npm create sanity@latest -- --env=.env.local --create-project "Vastralaya ecommerce" --dataset production
```

If you don’t have a Sanity account, this command will guide you to create one.
When prompted with "Would you like to add configuration files for a Sanity project in this Next.js folder?", select "n" (no), as the --env=.env.local flag handles this automatically.
After running this command, a .env.local file will be created (or updated) in your project root with:
NEXT_PUBLIC_SANITY_PROJECT_ID: A unique ID for your Sanity project, generated during this step.
NEXT_PUBLIC_SANITY_DATASET: Set to production.

- Note: You can verify your NEXT_PUBLIC_SANITY_PROJECT_ID later by logging into https://www.sanity.io/manage, selecting the "Vastralaya ecommerce" project, and checking the project details.

## 3. Set Up Environment Variables

The application requires additional environment variables beyond those set in Step 2. Edit your .env file in the project root to include the following:

```bash

NEXT_PUBLIC_BASE_URL=http://localhost:3000
NEXT_PUBLIC_SANITY_PROJECT_ID=<already-set-by-step-2>
NEXT_PUBLIC_SANITY_DATASET=production
NEXT_PUBLIC_SANITY_API_VERSION=2024-11-09
SANITY_API_TOKEN=<your-sanity-api-token>
SANITY_API_READ_TOKEN=<your-sanity-api-read-token>
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=<your-clerk-publishable-key>
CLERK_SECRET_KEY=<your-clerk-secret-key>
STRIPE_SECRET_KEY=<your-stripe-secret-key>
STRIPE_WEBHOOK_SECRET=<your-stripe-webhook-secret>
SENDBIRD_APP_ID=<your-sendbird-app-id>

```

