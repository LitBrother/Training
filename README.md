# Private Marathon Planner

## Deploy to Cloudflare Pages
1. Create a private GitHub repository and upload these files.
2. In Cloudflare, open Workers & Pages, create a Pages project, and connect the repository.
3. Use no framework preset, no build command, and `/` as the output directory.
4. In the Pages project settings, add a Workers AI binding named `AI`.
5. Deploy the project.

## Protect with Cloudflare Access
1. Enable Zero Trust in Cloudflare.
2. Add a self-hosted Access application for the Pages production hostname and preview hostname.
3. Create an Allow policy restricted to your email address.
4. Test in a private browser window before entering personal training data.

## Data and AI
Progress and events use browser localStorage. Export a backup before changing device or clearing site data. AI requests send the entered context and six weeks of plan data to the `/api/coach` Pages Function. The deterministic rules continue to work if AI is unavailable.
