# Your website (free, 10 minutes)

Apple needs a **Privacy Policy URL** and a **Support URL**, and AdMob wants an
**app-ads.txt** file at the ROOT of your developer website. This folder covers all three.

Before uploading, replace `YOUR-EMAIL@example.com` in `index.html` and
`[YOUR EMAIL ADDRESS]` in `privacy.html` with your GAME email (it will be public).
`app-ads.txt` already contains your publisher ID (`pub-8100510255298322`).

## Option A (recommended): Netlify Drop - no account name or email shown
1. Go to https://app.netlify.com/drop (free; sign up with your game email).
2. Drag the contents of this `website` folder onto the page.
3. Netlify gives you a random address like `https://something-random.netlify.app`.
   In Site settings -> Change site name, make it `pocketlion26`
   -> `https://pocketlion26.netlify.app`.
4. Check `https://pocketlion26.netlify.app/app-ads.txt` loads.

## Option B: GitHub Pages under a free ORGANIZATION
GitHub's terms allow one free personal account per person, so don't make a second
personal account. Instead, inside your existing account create a free **Organization**
called `PocketLion26`, then a PUBLIC repository named `pocketlion26.github.io` in it,
upload these files, and enable Settings -> Pages (branch `main`, root).
Set your Git commit email to GitHub's private `noreply` address (Settings -> Emails ->
"Keep my email addresses private"), and keep org membership private.
Anyone can see a public repo's files and history, so only ever upload what is in this folder.

## In App Store Connect
- Marketing URL / Support URL: your site root
- Privacy Policy URL: your site root + `/privacy.html`
- AdMob -> Apps -> Arcade Ascent -> app-ads.txt: check it is found (can take up to a day)

## Option B in detail: GitHub Pages from your Organization
1. On the "Create a new repository" page, set **Owner** to your organization
   (PocketLion26), NOT your personal account.
2. **Repository name:** exactly `pocketlion26.github.io` (all lowercase).
3. Choose **Public** (free Pages needs a public repository). Leave everything else as is,
   click **Create repository**.
4. On the new empty repo page click **uploading an existing file**. Drag in the FILES
   from this folder (`index.html`, `privacy.html`, `app-ads.txt`), not the folder itself.
   Click **Commit changes**.
5. Open the repo's **Settings -> Pages**. Under Build and deployment choose
   **Deploy from a branch**, branch **main**, folder **/ (root)**, click **Save**.
6. Wait 1-10 minutes, then open `https://pocketlion26.github.io` and
   `https://pocketlion26.github.io/app-ads.txt` to check both load.
7. Privacy: in your personal GitHub **Settings -> Emails** tick "Keep my email addresses
   private", and in the organization's **People** page set your membership to Private.

## One website for all your games
Yes, one site is enough. Apple and AdMob only need URLs, and the same URLs can be
used for every game:
- **Privacy policy:** `privacy.html` says it covers "the games published by PocketLion26",
  and includes a section on in-app purchases (currency / DLC) handled by Apple. It stays
  accurate as long as your games only use AdMob and Apple purchases. If a game adds
  anything else (accounts, analytics, a server, another ad network or purchase service),
  update the policy before releasing it.
- **Support page / marketing URL:** the site root works for all games. Optionally add a
  page per game (e.g. `arcade-ascent.html`) and link them from `index.html`.
- **app-ads.txt:** one file at the site root. All your games under the same AdMob
  account share the same publisher ID, so you never need to change it.
