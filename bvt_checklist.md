# Build Verification Test (BVT) Checklist - Epic Ocean Guide

This checklist acts as a Smoke Test to quickly verify if a newly deployed website build is stable enough for deeper, comprehensive testing. 

---

## BVT Test Suite Matrix

| Section | Title | Preconditions | Steps | Expected Result | Priority | Type |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Availability & Deployment** | Verify server response status (200 OK) | Internet connection, stable build deployed. | 1. Open the browser.<br>2. Navigate to 'https://www.epicoceanguide.com/'.<br>3. Check the HTTP response status code in Network tab. | The server returns an HTTP status code 200 OK. The homepage loads completely. | Critical | Automated |
| **Availability & Deployment** | Verify absence of critical server errors (5xx/4xx) | Website URL is accessible. | 1. Open 'https://www.epicoceanguide.com/'.<br>2. Navigate through 2-3 top-level categories.<br>3. Observe the pages for unexpected error messages. | No '500 Internal Server Error', '502 Bad Gateway', or blank screen issues are encountered. | Critical | Functional |
| **Availability & Deployment** | Verify application build version | Access to the website. | 1. Scroll to the footer or inspect the page source/meta tags.<br>2. Locate the current build version or commit hash. | The version matches the latest release/deployment ticket number. | Low | Other |
| **Critical Core Functionality** | Verify core layout rendering and main navigation | Website homepage is loaded. | 1. Check if header, main content block, and footer are rendered.<br>2. Click on a main category link (e.g., Guides/Destinations). | The core layout structure renders correctly. Navigation link successfully takes the user to the destination page. | Critical | Functional |
| **Critical Core Functionality** | Verify search bar responsiveness | Website homepage is loaded. | 1. Click on the search input field.<br>2. Type a basic test term (e.g., 'ocean').<br>3. Press Enter or click the Search button. | The search action triggers successfully and redirects the user to a search results page without freezing. | High | Functional |
| **Key Integrations & Forms** | Verify newsletter/lead form submission | A valid test email address. | 1. Scroll to the newsletter subscription block.<br>2. Enter a valid test email address.<br>3. Click the submit/subscribe button. | The form submits successfully. A success message or validation confirmation is displayed to the user. | High | Functional |
| **Browser Console Check** | Verify browser console for critical JavaScript errors | Website homepage is loaded. | 1. Right-click on the page and select 'Inspect' (or press F12).<br>2. Navigate to the 'Console' tab.<br>3. Check for red error indicators. | There are no critical 'Uncaught' exceptions or JavaScript crashes that block core user interactions. | High | Other |
