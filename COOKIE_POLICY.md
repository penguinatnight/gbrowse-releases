# Gbrowse Cookie, Local Storage & Tracking Policy

**Effective Date:** October 8, 2026  
**Last Updated:** October 8, 2026  
**Version:** 1.0  
**Application:** Gbrowse Desktop Application (Windows)  
**Publisher:** Yab Studios  
**License Model:** Proprietary Freeware (Closed Source)  
**Primary Contact:** legal@yabstudios.com  
**Official Website:** https://yabstudios.com  

---

### 1. OVERVIEW: A LOCAL-FIRST PRIVACY UTILITY

Gbrowse is a desktop browser profile management workstation engineered from inception around the foundational principles of **local data sovereignty**, **zero telemetry**, and **strict storage isolation**. 

Unlike web applications, SaaS platforms, or cloud-synced multi-account browsers, Gbrowse is a **local-first desktop program**. The application binary runs exclusively on your local computer hardware and does not operate remote telemetry tracking, user analytics harvesting, or advertising pixels.

This Policy explains clearly and transparently:
1. Why the Gbrowse desktop client itself does **not** deploy HTTP cookies, web beacons, or tracking technologies;
2. How third-party browser profiles you configure and launch through Gbrowse isolate web cookies locally on your device;
3. How you maintain absolute control over the storage, retention, and deletion of all local browser data.

---

### 2. ZERO COOKIES AND TRACKING IN THE GBROWSE DESKTOP CORE

2.1 **Zero Application Cookies.** The Gbrowse desktop application (built with Rust and Tauri 2) is a native desktop client. It does **not** set, read, or transmit HTTP cookies, tracking cookies, Flash cookies (LSOs), HTML5 local storage beacons, or canvas fingerprinters to monitor your usage of the application.

2.2 **Zero Telemetry & Analytics Beacons.** Gbrowse does **not** bundle or execute background analytics software development kits (SDKs), advertising surveillance pixels, or behavioral monitoring scripts (such as Google Analytics, Segment, Mixpanel, Sentry telemetry, or Meta Pixels). We do not record:
- What websites or URLs you visit in your profiles;
- Your profile names, tags, or organizational folder hierarchies;
- Your browsing session durations, frequency, or keystrokes;
- Your search queries or browser history.

2.3 **Hardware DPAPI Encryption for Credentials.** All sensitive credentials you choose to enter into Gbrowse (such as proxy passwords and authentication tokens) are encrypted locally using the Windows Operating System Data Protection API (DPAPI) via `CryptProtectData`. These credentials are never packaged into cookies, never written in plaintext, and never transmitted outside your local machine.

---

### 3. CONTAINERIZED THIRD-PARTY COOKIES IN LAUNCHED PROFILES

When you use Gbrowse to launch isolated browser profiles (Google Chrome, Chromium, Mozilla Firefox, Microsoft Edge, or Apple Safari container modes), it is important to understand how cookies function from a technical architecture standpoint:

3.1 **External Websites Set Third-Party Cookies.** When you navigate to external websites and web applications (e.g., `google.com`, `tiktok.com`, `amazon.com`, `reddit.com`) inside a launched browser profile, *those external websites* issue HTTP cookies (`Set-Cookie` headers), IndexedDB databases, session tokens, and local storage items to your browser. These cookies are created and dictated exclusively by the third-party websites you choose to visit, not by Gbrowse.

3.2 **Strict Local Partitioning (Zero Session Bleed).** In a standard consumer browser, cookies and session caches are shared globally across tabs. Gbrowse enforces strict, containerized storage separation:
- Every profile created in Gbrowse is assigned a unique UUID and a completely isolated directory on your local disk:
  ```text
  %APPDATA%\gbrowse\profiles\<profile-uuid>\
  ```
- All cookies, cache files, local storage, service worker registrations, and IndexedDB files generated during your browsing sessions are saved strictly within that profile's dedicated directory.
- Profile A cannot access, read, or bleed cookies into Profile B.
- **Gbrowse developers do NOT have access to, cannot inspect, and do NOT synchronize or upload these third-party cookies to any cloud server.**

3.3 **Governed by Third-Party Privacy Policies.** Any cookies placed on your machine by third-party websites during your browsing sessions are governed strictly by the privacy policies, cookie policies, and terms of service of those respective external websites. We encourage you to review the privacy disclosures of every website you visit.

---

### 4. YOUR RIGHTS AND DATA SOVEREIGNTY: MANAGING AND DELETING COOKIES

Because all browser cookies and storage files reside entirely on your physical storage drive, you have complete and instantaneous control over their retention and destruction:

4.1 **Per-Profile Cookie Clearing & Deletion:**
- You can clear browsing data and cookies directly inside any active browser profile using standard browser settings (`Ctrl+Shift+Delete`).
- Deleting a profile from within the Gbrowse user interface permanently deletes the profile directory on your disk, instantaneously destroying all cookies, cached files, and local session stores associated with that profile.

4.2 **Complete Purge:**
To permanently purge all local cookies, caches, and profile records across all profiles, you can delete the root storage folder located at:
```text
%APPDATA%\gbrowse\profiles
```

---

### 5. REGULATORY COMPLIANCE (ePrivacy Directive & GDPR)

Under Article 5(3) of the European Union ePrivacy Directive (Directive 2002/58/EC as amended), storing information or gaining access to information stored in the terminal equipment of a subscriber or user requires informed consent, unless strictly necessary to provide an information society service explicitly requested by the user.

Because Gbrowse:
(a) Does not set or read tracking cookies on your device;
(b) Does not harvest or monetize terminal equipment data; and
(c) Stores browser profile files locally solely as a technical necessity to fulfill your explicit instruction to maintain persistent browser containers,

Gbrowse adheres to the highest European privacy-by-design standards without requiring deceptive or disruptive cookie banners.

---

### 6. CONTACT INFORMATION

If you have any questions or inquiries regarding our Cookie, Local Storage, and Tracking Policy, please contact us at:

* **Entity:** Yab Studios  
* **Primary Contact:** Yab Studios Privacy & Compliance  
* **Legal Email:** legal@yabstudios.com  
* **Support Email:** support@yabstudios.com  
* **Official Website:** https://yabstudios.com  
