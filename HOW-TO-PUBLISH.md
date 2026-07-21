# Yes We Travel Too — How to Publish & Manage Your Site

## YOUR SITE FILES AT A GLANCE

```
yes-we-travel-too/
├── index.html          ← Homepage
├── about.html          ← About page
├── blog.html           ← All posts listing
├── places.html         ← Places Traveled page
├── contact.html        ← Contact page
├── 404.html            ← Page not found
├── style.css           ← All styling (colors, fonts, layout)
├── netlify.toml        ← Netlify settings — don't touch
├── NEW-POST-TEMPLATE.html  ← COPY THIS for every new post
├── post-nairobi.html   ← Example post
├── post-lisbon.html    ← Example post
├── post-nola.html      ← Example post
└── images/
    └── (upload all your photos here)
```

---

## FIRST-TIME SETUP (do this once)

### Step 1 — Create a GitHub account
1. Go to **github.com** and sign up (free)
2. Confirm your email

### Step 2 — Create your repository
1. Click the **+** icon (top right) → **New repository**
2. Name it: `yes-we-travel-too`
3. Set to **Public**
4. Click **Create repository**

### Step 3 — Upload your site files
1. On your new empty repository page, click **uploading an existing file**
2. Drag ALL your site files and the `images` folder into the upload area
3. Scroll down, click **Commit changes**
4. Wait a few seconds — your files will appear in the repository

### Step 4 — Connect to Netlify
1. Go to **netlify.com** and sign up with your GitHub account
2. Click **Add new site** → **Import an existing project**
3. Choose **GitHub**
4. Select your `yes-we-travel-too` repository
5. Leave all settings as defaults
6. Click **Deploy site**
7. In about 30 seconds, Netlify gives you a URL like `random-name-123.netlify.app`

### Step 5 — Set your custom Netlify subdomain (optional but recommended)
1. In Netlify → **Site settings** → **Domain management**
2. Click **Options** → **Edit site name**
3. Change it to: `yeswetraveltoo` → your site becomes `yeswetraveltoo.netlify.app`

**That's it. Your site is live.**

From now on, any file you change on GitHub automatically deploys to your live site within 60 seconds — no re-uploading, no zipping.

---

## HOW TO ADD A NEW BLOG POST

### Step 1 — Copy the template
In your GitHub repository:
1. Click on `NEW-POST-TEMPLATE.html`
2. Click the **Copy raw file** icon (two overlapping squares, top right)
3. Go back to your repository home
4. Click **Add file** → **Create new file**
5. Name it something like `post-cape-town.html` (use hyphens, no spaces)
6. Paste the template content in

### Step 2 — Fill in your post
Edit these parts of the template (search for the STEP comments):
- **STEP 1**: Update the `<title>` tag
- **STEP 2**: Update the meta description  
- **STEP 3**: Update the category and headline
- **STEP 4**: Update date and destination
- **STEP 5**: Add your hero photo or keep the emoji placeholder
- **STEP 6**: Write your post content
- **STEP 7**: Update the tags
- **STEP 8**: Update the "Next post" link

### Step 3 — Upload your photos
1. In your GitHub repository, click on the `images` folder
2. Click **Add file** → **Upload files**
3. Drag in your photos (named with hyphens, no spaces — e.g. `cape-town-waterfront.jpg`)
4. Click **Commit changes**

To use a photo in your post, reference it like this in the HTML:
```html
<img src="images/cape-town-waterfront.jpg" alt="Cape Town waterfront at sunset" class="post-img"/>
```

### Step 4 — Add it to the Blog page
1. Open `blog.html` in GitHub (click the file, then the pencil ✏️ icon to edit)
2. Find an existing post card block that looks like this:
```html
<a href="post-nairobi.html" class="post-card">
  ...
</a>
```
3. Copy that entire block (from `<a href=` to `</a>`)
4. Paste it at the TOP of the posts grid (so newest posts appear first)
5. Update the link, emoji, label, date, title, and excerpt to match your new post
6. Click **Commit changes**

### Step 5 — Done!
Netlify detects the change and deploys automatically. Your post is live in under 60 seconds.

---

## HOW TO EDIT EXISTING PAGES

1. Go to your GitHub repository
2. Click on the file you want to edit (e.g., `about.html`)
3. Click the **pencil icon** (✏️) — top right of the file view
4. Make your changes directly in the browser
5. Click **Commit changes** (green button, bottom of page)
6. Your site updates automatically

---

## HOW TO ADD YOUR OWN PHOTOS TO THE HOMEPAGE

The homepage currently shows example destinations (Nairobi, Lisbon, New Orleans). To add your own:

1. Open `index.html` for editing
2. Find the `passport-stack` section (search for "passport-stack")
3. Update the emoji, city name, and date in each `passport-card`
4. Find the `stamp-grid` section (search for "stamp-grid")  
5. Update each `stamp-tile` with your actual destinations

---

## HOW TO MONETIZE (when you're ready)

### Google AdSense
1. Sign up at **google.com/adsense**
2. Add your site URL and get approved (takes a few days)
3. Google gives you a small `<script>` tag — add it inside `<head>` in every HTML file
4. Add this where you want ads to appear in posts:
```html
<div class="ad-unit">
  <!-- Paste your AdSense ad unit code here -->
</div>
```

### Affiliate Links
Simply replace any link with your affiliate link. Example for Amazon Associates:
```html
<a href="https://amazon.com/your-affiliate-link" target="_blank" rel="noopener sponsored">
  The packing cubes I use on every trip
</a>
```

### Booking.com Affiliate
Sign up at **partners.booking.com** — get a link for any hotel/destination and paste it into your posts wherever you mention accommodation.

---

## HOW TO USE A CUSTOM DOMAIN (e.g., yeswetraveltoo.com)

1. Buy your domain at **Namecheap** or **Squarespace Domains** (~$15/year)
2. In Netlify → **Domain management** → **Add custom domain**
3. Follow the DNS instructions (Netlify walks you through it step by step)
4. Free HTTPS/SSL is included automatically

---

## QUICK TIPS

- **Compress photos before uploading** — use squoosh.app (free, in your browser). Large photos slow your site down.
- **Name photos with hyphens** — `cape-town-sunset.jpg` not `Cape Town Sunset.jpg`
- **Backup your work** — GitHub is your backup. Every change is saved in version history.
- **Preview before committing** — paste your HTML into htmlpreview.github.io to check it looks right before saving to GitHub.
