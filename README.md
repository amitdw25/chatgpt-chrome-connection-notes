# ChatGPT Chrome connection: errors and observed recovery

Personal troubleshooting record by Amit Dwivedi. Updated 17 October 2026 (IST). This is a user experience report, not an official fix or an issue submitted to OpenAI.

## Problem
On Windows, ChatGPT desktop/browser control stopped working after a Windows update (user-reported timing; causation unconfirmed). Opening Chrome tabs and reading pages failed.

Errors encountered across attempts:
- `Sheep MCP session closed: RPC INTERNAL`
- `Unable to find connected browser`
- `failed to launch codex app-server: program not found`
- `Codex app-server manifest missing nodePath`
- `Windows platform directly not found` (reported wording)
- `MCP request timed out`

## Attempts before recovery
The user reported trying Windows and Chrome updates, Chrome reinstallation, extension removal/reinstallation, desktop app repair/reinstallation, ending app processes, resetting browser control, and an Edge test. These attempts did not produce a confirmed lasting recovery at the time.

## What worked in this session
On 17 October 2026, at approximately 12:18 IST, the user granted the browser permission prompt. The browser connection then responded successfully. A new blank Chrome tab was created and verified as `about:blank`. Later, an existing WhatsApp Web tab was read and a user-authorized test message was sent successfully at approximately 12:23 IST. GitHub navigation and profile editing also worked afterward.

Practical recovery sequence observed:
1. Open ChatGPT Work in Chrome with the browser extension available.
2. Request a simple browser action.
3. Grant the browser permission prompt when it appears.
4. Retry the action and verify that a new tab actually opens.

## Status and limits
**Browser control recovered in the tested session. Root cause remains unconfirmed.** The exact permission prompt type was not recorded. Successful actions after permission approval do not prove permission was the sole cause or that every earlier error has the same cause. Desktop/native app control was not retested; long-term stability is unknown. No verified evidence establishes a broken system PATH or a need to install Node.js manually.

## हिंदी सार
समस्या: Windows update के बाद ChatGPT से Chrome control करते समय RPC INTERNAL, app-server और timeout errors आ रहे थे। कई repair/reinstall प्रयासों के बाद भी तत्काल पुष्टि नहीं हुई।

17 अक्टूबर 2026 को browser permission देने के बाद इसी session में connection चलने लगा। नया Chrome tab खुला और WhatsApp पर अधिकृत संदेश भेजा गया। यह काम दोबारा शुरू होने का देखा गया परिणाम है; मूल कारण और स्थायी समाधान की पुष्टि अभी नहीं हुई है।
