
# Firebase Studio

This is a NextJS starter in Firebase Studio.

To get started, take a look at src/app/page.tsx.

## Deployment

### Netlify

This project is ready to be deployed on Netlify.

1.  **Push to GitHub (or GitLab/Bitbucket)**:
    *   Create a new repository on your preferred Git provider.
    *   Initialize a Git repository in your project folder, commit your files, and push them.
    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    git remote add origin YOUR_REPOSITORY_URL
    git push -u origin main
    ```

2.  **Connect to Netlify**:
    *   Log in to your Netlify account.
    *   Click on "Add new site" -> "Import an existing project".
    *   Connect to your Git provider and select your repository.

3.  **Build Settings**:
    *   Netlify should automatically detect that this is a Next.js project and configure most build settings correctly.
    *   The `netlify.toml` file provides a base configuration.
    *   **Build command**: `next build`
    *   **Publish directory**: Netlify's Next.js runtime typically handles this automatically.

4.  **Environment Variables**:
    *   It is crucial to set up environment variables in the Netlify UI (Site settings -> Build & deploy -> Environment).
    *   `TELEGRAM_BOT_TOKEN`: Your Telegram bot token (currently in `src/config/site.ts`, but should be moved to an environment variable for production).
    *   `GOOGLE_API_KEY` (or `GEMINI_API_KEY`): If you use Genkit with Google AI models, you will need to provide an API key. The specific name of the variable depends on how `@genkit-ai/googleai` is configured to pick it up (often `GOOGLE_API_KEY` or `GEMINI_API_KEY`).

5.  **Deploy**:
    *   Click "Deploy site".

### Other Platforms

For other platforms like Vercel (recommended for Next.js), the deployment process is often similar, involving connecting your Git repository and configuring build settings and environment variables through their UI.
