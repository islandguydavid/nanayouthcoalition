# Publish Nanaimo Youth Coalition on Google Sites

`index.html` is the complete, portable website file. It includes its own CSS and small amount of JavaScript, so it does not need a separate style sheet or script file.

Google Sites supports embedded HTML/CSS/JavaScript and Google Forms, but it does not upload a standalone website project as the site itself. The most reliable way to preserve this complete design is to put `index.html` at a public HTTPS address first, then add it to Google Sites using **Insert → Embed → By URL**. You can also try **Insert → Embed → Embed code** and paste the HTML; if Google Sites removes document-level code or the layout appears constrained, use the URL embed route instead.

## Contact form: one owner action before go-live

The contact form uses FormSubmit and is configured to send inquiries to `jerry@bigscvi.ca`. FormSubmit sends a confirmation/activation email to that inbox on the first real submission. Jerry must open that email and approve it. After that one-time confirmation, the form can deliver future inquiries without a server or API key. FormSubmit then displays its own verification or confirmation page after a user submits; the site intentionally does not claim delivery before that provider response. The form includes browser-side required fields, a consent checkbox, FormSubmit's CAPTCHA, and a hidden honeypot field.

Before public launch, submit one test from the published page, approve the FormSubmit activation email, and then submit a second test to confirm delivery. If the coalition later has a dedicated mailbox, replace every `jerry@bigscvi.ca` occurrence in `index.html` with the new address, then repeat the activation test.

## Optional Google-native form route

If the coalition wants Google-native response storage instead, create a Google Form containing name, email, connection type, message, and consent. Publish it for the intended audience, link responses to a Google Sheet if wanted, then insert it in Google Sites with **Insert → Forms**. That option replaces the HTML contact block rather than using the current FormSubmit form.

## Image note

The hero plus the two supporting youth lifestyle photos already use public HTTPS URLs, so they will continue to display when the HTML is embedded or hosted elsewhere. If the coalition later has its own approved photography, replace the relevant `src` values; the designed teal graphic fallback remains visually complete if a photo is removed.

## Before connecting the domain

Set `nanaimoyouthcoalition.ca` to point to the host that serves the HTML (or use it as the Google Sites custom domain). Add a privacy link once the coalition has final privacy language, especially if the form will collect information from minors.

## Official Google guidance

- [Add Google files, videos, website content, and code in Google Sites](https://support.google.com/sites/answer/90569?hl=en)
- [Publish and share a Google Form with responders](https://support.google.com/docs/answer/2839588?hl=en)
- [Embed a deployed Apps Script web app in Google Sites](https://developers.google.com/apps-script/guides/web)
