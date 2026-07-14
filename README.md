# Finding Ocean Activities - QA Testing Checklists

This repository contains structured testing checklists for the **Epic Ocean Guide** website project (https://www.epicoceanguide.com/). These documents are ready for manual testing or reference in your learning/QA projects.

---

## 1. 🚀 Build Verification Test (BVT) Checklist
*This checklist acts as a Smoke Test to quickly verify if a newly deployed website build is stable enough for deeper testing.*

| Section | Title | Preconditions | Steps | Expected Result | Priority | Type |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Availability** | Verify server response status (200 OK) | Internet connection, stable build deployed. | 1. Open the browser.<br>2. Navigate to website.<br>3. Check the HTTP response status code in Network tab. | The server returns an HTTP status code 200 OK. The homepage loads completely. | Critical | Automated |
| **Availability** | Verify absence of critical server errors (5xx/4xx) | Website URL is accessible. | 1. Open website.<br>2. Navigate through 2-3 top-level categories.<br>3. Observe pages for unexpected error messages. | No '500 Internal Server Error', '502 Bad Gateway', or blank screen issues are encountered. | Critical | Functional |
| **Availability** | Verify application build version | Access to the website. | 1. Scroll to the footer or inspect the page source/meta tags.<br>2. Locate the current build version or commit hash. | The version matches the latest release/deployment ticket number. | Low | Other |
| **Core Functionality** | Verify core layout rendering and main navigation | Website homepage is loaded. | 1. Check if header, main content block, and footer are rendered.<br>2. Click on a main category link (e.g., Guides/Destinations). | The core layout structure renders correctly. Navigation link successfully takes the user to the destination page. | Critical | Functional |
| **Core Functionality** | Verify search bar responsiveness | Website homepage is loaded. | 1. Click on the search input field.<br>2. Type a basic test term (e.g., 'ocean').<br>3. Press Enter or click the Search button. | The search action triggers successfully and redirects the user to a search results page without freezing. | High | Functional |
| **Key Integrations** | Verify newsletter/lead form submission | A valid test email address. | 1. Scroll to the newsletter subscription block.<br>2. Enter a valid test email address.<br>3. Click the submit/subscribe button. | The form submits successfully. A success message or validation confirmation is displayed to the user. | High | Functional |
| **Console Check** | Verify browser console for critical JavaScript errors | Website homepage is loaded. | 1. Right-click on the page and select 'Inspect' (F12).<br>2. Navigate to the 'Console' tab.<br>3. Check for red error indicators. | There are no critical 'Uncaught' exceptions or JavaScript crashes that block core user interactions. | High | Other |

---

## 📋 2. Comprehensive Website Checklist
*A deep-dive comprehensive list covering Technical, UX/UI, SEO, and Analytics requirements.*

### 🛠️ Technical State & Speed (SEO & Performance)
- [ ] **Loading Speed:** Verify via Google PageSpeed Insights. Mobile score should be in the green zone, specifically checking Largest Contentful Paint (LCP).
- [ ] **Image Optimization:** All images compressed (WebP/AVIF format) and descriptive `alt` tags populated for SEO.
- [ ] **SSL Certificate:** Ensure HTTPS is active with a secure lock icon. Validate automated HTTP to HTTPS redirects.
- [ ] **Responsiveness:** Verify layouts across diverse mobile, tablet, and desktop screens. Text must remain readable without manual zoom; elements must not overlap.
- [ ] **Custom 404 Page:** Check that an invalid URL displays a branded, custom 404 error page containing an easy return link to the homepage.

### 🎨 Content & Structure (UX/UI)
- [ ] **Main Navigation:** Ensure intuitive structure enabling users to find any destination guide within 2-3 clicks max.
- [ ] **Favicon Presence:** Verify custom ocean-themed icon renders perfectly in the browser tab.
- [ ] **Clickable Contact Links:** Phone numbers (`tel:`), emails (`mailto:`), and social icons open up flawlessly (social media should use `target="_blank"`).
- [ ] **Internal Search Engine:** Test with keywords (e.g., 'diving', 'sharks') to verify relevancy and format stability on the results page.
- [ ] **Legal Footer Links:** Verify Privacy Policy and Terms of Service documents are updated and easily accessible from the footer.

### 🔍 Search Engine Optimization (SEO)
- [ ] **Meta Tags Verification:** Check that every target page has a unique `<title>` (under 60 chars) and `<meta name="description">` (150-160 chars).
- [ ] **Heading Hierarchy:** Validate that exactly one single `<h1>` tag represents the title per page, properly followed by sequential `<h2>` and `<h3>` tags.
- [ ] **Sitemap & Robots.txt:** Ensure correct production deployment of `sitemap.xml` and `robots.txt` files for search engine indexation.

### 📊 Analytics & Marketing
- [ ] **Google Analytics 4 (GA4):** Track scripts ensuring live traffic recording through the real-time reporting dashboard.
- [ ] **Google Search Console:** Verify that domain property verification is active and working.
- [ ] **Form Integrations:** End-to-end testing of data routing on newsletter fields to make sure the backend captures subscription strings correctly.
