# Overview:
Developers that maintain developer tools frequently have to write changelogs every few days updating end users (also developers). The end users typically see them on some type of public website. 

The challenge with writing changelogs is twofold:

1. You have to go through a few days of commits to make a list of everything that’s changed.
2. You have to summarize the changes that would be relevant to an end-user in a few bullet points.

# High Level Requirements:
1. A developer-facing tool that allows devs to quickly AI-generate a changelog.
2. A simple public-facing website where the changelog appears for people to see.

# Pages Info:
1. Main changelog page:
    - List of changelogs
    - Scrolling pagination, 5 changelogs at a time
2. Main developer dashboard repo:
    - Connect repo to github option
    - Set default number days of commits to summarize. 1 to 30.
    - Set tags to attach to every changelog
    - Gemini 2.0 flash for cost reasons
    

# Integrations
1. Connect a github repo to pull changelog data from upon connecting. Use polling.
2. Webhook that gets called whenever the repo gets pushed to, in order to update changelog
3. Vercel AI SDK

# AI parsing rules
- Configurable number of days worth of commits to summarize
- Need to make the prompt
- Only read commits that start with "feat\(" or "fix\(". Strip lines that have neither.

# Changelog format
- One line: Date range + Categories affected as badges
- Features
- Fixes