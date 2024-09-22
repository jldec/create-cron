README.md

```sh
~/cloudflare$ pnpm create cloudflare
 ╭──────────────────────────────────────────────────────────────╮
 │ 👋 Welcome to create-cloudflare v2.27.3!                     │
 │ 🧡 Let's get started.                                        │
 ╰──────────────────────────────────────────────────────────────╯
╭ Create an application with Cloudflare Step 1 of 3
│ 
├ In which directory do you want to create your application?
│ dir ./create-cron
│
├ What would you like to start with?
│ category Application Starter
│
├ Which template would you like to use?
│ type Scheduled Worker (Cron Trigger)
│
├ Which language do you want to use?
│ lang JavaScript
│
├ Copying template files 
│ files copied to project directory
│ 
├ Updating name in `package.json` 
│ updated `package.json`
│ 
├ Installing dependencies 
│ installed via `pnpm install`
│ 
╰ Application created 

╭ Configuring your application for Cloudflare Step 2 of 3
│ 
├ Retrieving current workerd compatibility date 
│ compatibility date 2024-09-19
│ 
├ Do you want to use git for version control?
│ yes git
│
├ Initializing git repo 
│ initialized git
│ 
├ Committing new files 
│ git commit
│ 
╰ Application configured 

╭ Deploy with Cloudflare Step 3 of 3
│ 
├ Do you want to deploy your application?
│ no deploy via `pnpm run deploy`
│
╰ Done 

 ╭──────────────────────────────────────────────────────────────╮
 │ 🎉  SUCCESS  Application created successfully!               │
 │                                                              │
 │ 💻 Continue Developing                                       │
 │    Change directories: cd create-cron                        │
 │    Start dev server: pnpm run start                          │
 │    Deploy: pnpm run deploy                                   │
 │                                                              │
 │ 📖 Explore Documentation                                     │
 │    https://developers.cloudflare.com/workers                 │
 │                                                              │
 │ 💬 Join our Community                                        │
 │    https://discord.cloudflare.com                            │
 ╰──────────────────────────────────────────────────────────────╯

~/cloudflare$ cd create-cron/

jurgen@jldec.me main ~/cloudflare/create-cron$ git log
commit a699d836b377889d68ed0f5f13e1edd83125915e (HEAD -> main)
Author: jldec <jurgen@jldec.me>
Date:   Sun Sep 22 22:10:23 2024 +0100

    Initial commit (by create-cloudflare CLI)
    
    Details:
      C3 = create-cloudflare@2.27.3
      project name = create-cron
      package manager = pnpm@9.11.0
      wrangler = wrangler@3.78.6
      git = 2.39.5 (Apple Git-154)

jurgen@jldec.me main ~/cloudflare/create-cron$ pnpm run deploy

> create-cron@0.0.0 deploy /Users/jldec/cloudflare/create-cron
> wrangler deploy

 ⛅️ wrangler 3.78.7
-------------------

Total Upload: 0.73 KiB / gzip: 0.45 KiB
Uploaded create-cron (3.82 sec)
Deployed create-cron triggers (5.88 sec)
  https://create-cron.jldec.workers.dev
  schedule: * * * * *
Current Version ID: 3704f509-8a69-43b1-8f7d-4714140bc357

jurgen@jldec.me main ~/cloudflare/create-cron$ jq .scripts < package.json
{
  "deploy": "wrangler deploy",
  "dev": "wrangler dev --test-scheduled",
  "start": "wrangler dev --test-scheduled"
}
```