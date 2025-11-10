# Instructions for Claude CLI

Hi Claude! Please help me update the placeholder URLs in this RunAtom website export.

## Task

Update the `index.html` file with my actual URLs:

### 1. Contact Form URL
Find and replace: `https://forms.gle/your-form-id`
Replace with: `[USER: PROVIDE YOUR GOOGLE FORM OR TYPEFORM URL HERE]`

### 2. Upwork Profile
Find: `href="#"` in the Upwork link section (near the footer)
Replace with: `href="[USER: PROVIDE YOUR UPWORK PROFILE URL]"`

### 3. LinkedIn Profile  
Find: `href="#"` in the LinkedIn link section (near the footer)
Replace with: `href="[USER: PROVIDE YOUR LINKEDIN PROFILE URL]"`

## Context

This is a single-page website for an AI automation consulting business. The index.html file is minified, so you'll need to:

1. Read the entire index.html file
2. Find the three placeholder URLs mentioned above
3. Replace them with the actual URLs I provide
4. Save the updated file

## Important Notes

- The HTML is minified (all on one line), so be careful with the replacements
- Make sure not to break any surrounding HTML tags or attributes
- The Upwork and LinkedIn links are in the footer section near `hello@runatom.com`
- The form URL appears in two places (both "Learn More" buttons should point to the same form)

## After Updates

Once you've updated the URLs, I can deploy this directly to GitHub Pages without any additional changes needed.

---

## Example Prompt for Claude CLI

```
Please update the index.html file with these URLs:

1. Contact form: https://forms.gle/ABC123XYZ
2. Upwork profile: https://www.upwork.com/freelancers/~01234567890abcdef
3. LinkedIn profile: https://www.linkedin.com/in/yourname

Make sure to replace both instances of the form URL (in both "Learn More" buttons).
```
