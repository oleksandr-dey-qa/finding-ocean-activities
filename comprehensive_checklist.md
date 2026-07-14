# Comprehensive Website Checklist - Epic Ocean Guide

A deep-dive comprehensive testing checklist covering Technical, UX/UI, SEO, and Analytics requirements for the [Epic Ocean Guide](https://www.epicoceanguide.com/) website.

---

## 1. Technical State & Speed (SEO & Performance)
- [ ] **Loading Speed:** Verify website performance using Google PageSpeed Insights. Ensure the Mobile score is in the green zone, paying close attention to Largest Contentful Paint (LCP).
- [ ] **Image Optimization:** Check that all ocean graphics and travel images are compressed (ideally using modern formats like WebP or AVIF) and that each image contains a descriptive `alt` tag for SEO.
- [ ] **SSL Certificate:** Ensure HTTPS is fully active with a valid secure lock icon in the browser address bar. Validate that HTTP traffic automatically redirects to HTTPS.
- [ ] **Responsiveness:** Test layouts thoroughly across multiple viewports (mobile, tablet, desktop). Ensure elements do not overlap, text is readable without zooming, and buttons are easy to tap.
- [ ] **Custom 404 Page:** Input an invalid URL structure to confirm a custom, themed 404 page is loaded. Ensure it includes a clear, working link back to the homepage.

## 2. Content & Structure (UX/UI)
- [ ] **Main Navigation:** Verify the main menu structure is intuitive, allowing users to find any specific guide or sub-category (e.g., Destinations -> Atlantic Ocean) within 2-3 clicks.
- [ ] **Favicon Presence:** Ensure a custom ocean-themed favicon (e.g., wave, anchor, or trident) renders correctly on the browser tab.
- [ ] **Clickable Contacts:** Confirm that contact email addresses trigger `mailto:` links, phone numbers trigger `tel:` links, and social media links open the correct profiles in a new tab (`target="_blank"`).
- [ ] **Internal Search Engine:** Test the search functionality using specific keywords (e.g., 'diving', 'sharks'). Ensure results are relevant and do not distort the page layout.
- [ ] **Legal Footer Links:** Verify that links to the Privacy Policy and Terms of Service documents are clearly visible in the footer and lead to active, correct content pages.

## 3. Search Engine Optimization (SEO)
- [ ] **Meta Tags Verification:** Confirm every target page has a unique `<title>` tag (under 60 characters) and a `<meta name="description">` tag (between 150-160 characters).
- [ ] **Heading Hierarchy:** Inspect elements to ensure exactly one `<h1>` tag exists per page (the article title). Sub-headings must follow a logical sequence (`<h2>`, then `<h3>`) without skipping levels.
- [ ] **Sitemap & Robots.txt:** Validate that `sitemap.xml` and `robots.txt` are live on production, free of errors, and fully accessible to search engine crawlers.

## 4. Analytics & Marketing
- [ ] **Google Analytics 4 (GA4):** Confirm that the GA4 tracking script fires correctly on all pages by verifying live traffic in the real-time Google Analytics dashboard.
- [ ] **Google Search Console:** Ensure that the domain property is successfully verified and active within the Search Console console.
- [ ] **Form Integrations:** Perform end-to-end testing of newsletter subscription and contact forms. Verify success messages appear on the UI and submission strings are correctly captured in the database or CRM.
