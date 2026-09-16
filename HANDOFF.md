# Managing the Vintage Books "What's On" Events Page

This is a plain-English guide for whoever takes over updating the events page.
You do **not** need to know how to code. You update the page by **talking to
Claude**, the same way the page has been maintained so far.

- **The live page:** https://vintagebooks-events.netlify.app/
- **How it's run:** the page lives in a GitHub "repository" (a folder in the
  cloud). When a change is saved to GitHub, Netlify automatically rebuilds and
  publishes the live page within a minute or two. You never touch code directly —
  you ask Claude, and Claude makes the change and publishes it.

---

## 1. Accounts to sign up for

Create free accounts for all three. Use an email you check regularly.

| Service | Why you need it | Cost |
|---|---|---|
| **Claude** (https://claude.ai) | This is how you actually make changes — you chat with Claude and it edits and publishes the page. | **Paid plan required** (Claude Pro or higher). "Claude Code," the part that connects to the website's files, is included with a paid plan. |
| **GitHub** (https://github.com) | Where the website's files live. You'll be added as a collaborator so Claude (acting on your behalf) can save changes. | Free |
| **Netlify** (https://netlify.com) | What publishes the live page. Day to day you rarely need to open it, but you should have access in case the address or publishing settings ever need attention. | Free |

**Sign-up tip:** when you create the GitHub and Netlify accounts, you can click
"Sign up with Google" and use the same Google account for both — fewer passwords
to remember.

---

## 2. What the owner (Nelson) does to give you access

Send Nelson the **email address / username** you used for GitHub and Netlify.
He will:

1. **GitHub** — add you as a **collaborator** on the `vintage-books-events`
   repository (with write access), and accept means you'll get an email
   invitation — click the link to accept it.
2. **Netlify** — add you as a **member** on the site so you can see it in your
   dashboard.
3. **Claude GitHub connection** — make sure the **Claude GitHub App** has access
   to the `vintage-books-events` repository. This is the piece that lets Claude
   save your changes. If it's ever missing, Claude will tell you it "doesn't have
   GitHub access" — see Troubleshooting below.

---

## 3. How to make a change (the everyday routine)

1. Go to **https://claude.ai/code** (Claude Code on the web) and open the
   `vintage-books-events` project. (First time: you'll connect your GitHub
   account and pick this repository.)
2. **Type what you want in plain English.** Claude does the rest — edits the
   page, publishes it, and confirms when it's live.
3. Wait a minute, then refresh the live page to see it.

**If your change involves a new flyer image:** upload the image file to GitHub
first (in the `assets/flyers` folder — Nelson can show you the "Add file →
Upload files" button once), then tell Claude something like *"I uploaded a new
Summer Soirée flyer, please swap it in."* Claude finds it and wires it up.

---

## 4. Things you can just ask for (examples)

You don't need special wording — talk normally. Real examples that have worked:

- "Swap out the old flyers with the new ones and remove anything that's past."
- "Change the Monday reserve button to this link: <paste link>"
- "Trivia is every other Thursday now."
- "Add a new event — here are the details from the flyer…"
- "Write SOLD OUT on the Spooky Stories event."
- "The hours changed — we're open 4 PM daily, until midnight Fri–Sat."

Claude will make the change and push it live automatically.

---

## 5. Good to know

- **Saving = publishing.** Every change Claude makes goes to the live site
  (the `main` branch). There's no separate "publish" step to remember.
- **You can't really break it.** Every change is saved in history and can be
  undone. If something looks wrong, ask Claude to revert it.
- **Flyers update in place.** If you re-upload a flyer with the same filename,
  the new image shows up right away.
- **Event flyers** live in `assets/flyers/`. The file
  `assets/flyers/README.txt` lists which flyer belongs to which event.

---

## 6. Troubleshooting

- **"Claude doesn't have GitHub access…"** — the Claude GitHub App lost access to
  the repository. Fix: an admin re-adds the repo to the Claude GitHub App
  (https://github.com/apps/claude/installations/select_target) or reconnects
  GitHub in claude.ai settings. Make sure `vintage-books-events` is **checked**
  in the app's repository list. Then tell Claude "try again."
- **A change didn't show up on the live page** — wait 1–2 minutes and refresh;
  Netlify needs a moment to publish. If it's still off, ask Claude to confirm it
  pushed the change.
- **Anything you're unsure about** — reach out to **Nelson**
  (nelson.schnebelen@gmail.com) for support.

---

*This page is maintained through Claude. When in doubt, just ask Claude in plain
language — describe what you want changed and it will handle the rest.*
