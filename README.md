# Dash Porter MD — Website Setup Guide

## Files in this folder
- `index.html` — Home page
- `cv.html` — CV page (password protected)
- `contact.html` — Contact page

---

## Step 1: Add your photos

Open `index.html` in a text editor (TextEdit on Mac, Notepad on Windows).

Find the section that says `<!-- PHOTO INSTRUCTIONS -->` and replace each placeholder block like this:

**Before:**
```html
<div class="photo-slot">
  <div class="placeholder">Photo 1<br>Headshot</div>
</div>
```

**After:**
```html
<div class="photo-slot">
  <img src="headshot.jpg" alt="Dr. Dash Porter">
</div>
```

Place your image files in the same folder as the HTML files. Use simple filenames with no spaces (e.g. `headshot.jpg`, `outdoors1.jpg`).

---

## Step 2: Set up the Contact Form (Free)

1. Go to **https://formspree.io** and create a free account
2. Click "New Form" — give it a name like "Dash Porter Contact"
3. You'll get a form ID that looks like: `abcd1234`
4. Open `contact.html` and find this line:
   ```
   action="https://formspree.io/f/YOUR_FORMSPREE_ID"
   ```
5. Replace `YOUR_FORMSPREE_ID` with your actual ID:
   ```
   action="https://formspree.io/f/abcd1234"
   ```

Messages will be forwarded to your email. Free plan allows 50 submissions/month.

---

## Step 3: Host on GitHub Pages (Free)

1. Go to **https://github.com** and create a free account
2. Click "New Repository"
3. Name it exactly: `yourusername.github.io` (use your GitHub username)
4. Upload all your files (index.html, cv.html, contact.html, and photos)
5. Go to Settings → Pages → set Source to "main branch"
6. Your site will be live at: `https://yourusername.github.io`

### To use your own domain (dashporter.com or similar):
- In GitHub Pages settings, enter your custom domain
- In your domain registrar (wherever you bought the domain), add a CNAME record pointing to `yourusername.github.io`

---

## CV Password

The current password is: **drporter**

To change it, open `cv.html`, find this line:
```javascript
const CORRECT_PASSWORD = "drporter";
```
And replace `drporter` with your new password.

---

## HIPAA Note

The contact form includes a disclaimer and only collects professional inquiry information. Do not use this form for patient communications. If you ever want to add a patient-facing feature, a HIPAA-compliant form provider (like JotForm HIPAA or Formstack) would be required.
