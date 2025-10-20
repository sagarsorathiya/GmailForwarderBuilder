# Gmail → Telegram/WhatsApp Script Builder (Full)

Standalone GUI that generates Google Apps Script code to forward selected Gmail threads to Telegram bots or the WhatsApp Cloud API.

## Features
- Telegram and WhatsApp support with built-in token validators.
- Flexible Gmail filters: label, sender, subject, body preview length, and attachment workflow.
- Markdown-friendly formatting and optional Drive links for attachments.
- Quick setup and detailed guides embedded in the app.
- Tooltips across the form plus direct `getUpdates` fetch helper for discovering Telegram chat IDs.
- Packaged executable includes attribution for Sagar Sorathiya.

## Requirements
- Windows 10/11 (64-bit) with internet access.
- Google account with Gmail and Google Apps Script access.
- Telegram bot token / chat ID or WhatsApp Cloud API credentials.

## Installing & Launching
1. Download `GmailForwarderBuilder.exe` from the `dist/` folder.
2. Place the executable alongside `mail_to_telegram.ico` if you prefer the custom icon in Explorer.
3. Double-click to launch. If SmartScreen warns you, choose “More info” → “Run anyway”.

## Using the Builder
1. **Pick the target**: Telegram Bot or WhatsApp Cloud API.
2. **Fill credentials**:
   - Telegram: paste BotFather token, optionally validate, then click **Fetch IDs** after messaging your bot to get chat IDs.
   - WhatsApp: access token, phone number ID, and recipient number (international format).
3. **Set Gmail filters**:
   - Provide a label such as `SendToTelegram` (recommended) or leave blank to rely on sender/subject filters.
   - Combine multiple senders or subjects with Gmail OR syntax, e.g. `(alice@example.com OR bob@example.com)`.
   - Adjust body preview length if you want shorter/longer snippets.
4. Click **Generate Script**. Review the Apps Script shown on the right.
5. Use **Copy to Clipboard** or **Save as .gs file**.

## Deploying the Apps Script
1. Open <https://script.google.com> and create a new project.
2. Replace the default code with the generated script and save.
3. Run `sendFilteredEmailToChat` once; grant permissions for Gmail, Drive, and external HTTP requests.
4. Create a time-driven trigger (e.g., every 5 minutes) for `sendFilteredEmailToChat`.
5. Test by labelling an email or sending one that matches your filters; confirm delivery in Telegram/WhatsApp.

## Tips
- Use `@get_id_bot` or the Fetch IDs button to find chat IDs quickly.
- Attachments template stores files in Drive with public view links; ensure Drive sharing policies permit this.
- Monitor Apps Script > Executions for quota errors.
- To pause forwarding temporarily, disable the trigger instead of editing the script.

## Support & Credit
Created by [Sagar Sorathiya](https://github.com/sagarsorathiya). Report issues via the project repository or open an issue referencing the executable build.
