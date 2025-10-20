# Gmail Forwarder Builder

Welcome! This page provides the essentials for downloading and deploying the Gmail → Telegram/WhatsApp Script Builder.

## Download
- [Download the latest build](../GmailForwarderBuilder.exe) (Windows 64-bit)

## What It Does
This desktop helper generates Google Apps Script code that forwards filtered Gmail threads into Telegram or WhatsApp Cloud API conversations. Highlights include:
- Token validators for Telegram bots and WhatsApp Cloud API.
- Gmail label, sender, and subject filters with support for multiple values via Gmail OR syntax.
- Attachment-friendly workflow (optional) with Drive links.
- Built-in quick-start guide and tooltips for every input.

## Quick Start
1. Launch the executable and choose your target platform (Telegram or WhatsApp).
2. Paste your credentials and click **Fetch IDs** to find Telegram chat IDs if needed.
3. Configure Gmail filters (label recommended). Use patterns like `(alice@example.com OR bob@example.com)` for multiple senders.
4. Generate the Apps Script, copy it, and paste it into <https://script.google.com/>.
5. Authorize and schedule the script with a time-based trigger.

## Support & Credit
Created by [Sagar Sorathiya](https://github.com/sagarsorathiya). For questions or issues, open a ticket on the [GitHub repository](https://github.com/sagarsorathiya/GmailForwarderBuilder).
