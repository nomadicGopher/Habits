> [!IMPORTANT]
> Habits is in a pre-alpha state, and only suitable for use by developers.
> 
> **Progress to MVP**  
> ░░░░░░░░░░ (0%) <!--█-->

<!--[**Kanban Board**]()--> <!-- TODO: Copy GitHub project (LiberaDebt) & replace. -->

### To Do <!--[X]-->
* [ ] [Install Deno 2](https://github.com/denoland/deno?tab=readme-ov-file)
* SQLite for local DB
  * Save & upload (overwrite) features

1. SQLite in the Browser
You can use SQLite compiled to WebAssembly (WASM) to run SQLite entirely in the browser. Some popular options:

sql.js: SQLite compiled to WebAssembly.
wa-sqlite: A more modern and performant WASM SQLite implementation.
These allow you to:

Load a .sqlite file from local storage or user upload.
Query and update the database in the browser.
Save changes back to the file and offer it for download.
2. Accessing Files on Mobile Devices
PWAs can use:

File input (<input type="file">) to let users upload a .sqlite file.
File System Access API (limited support on mobile) to read/write files more directly.
IndexedDB or localStorage to persist data between sessions.
3. Storing the SQLite DB on the Device
You can:

Let the user upload a .sqlite file from their device.
Store it in memory or IndexedDB.
Allow them to download the updated file back to their device.
❌ Limitations
Direct file system access on mobile browsers is very limited.
Persistent storage is sandboxed and not shared with other apps.
No direct access to native SQLite databases used by other mobile apps (like WhatsApp or Notes).
🧠 Architecture Idea
Frontend (PWA):

Uses sql.js to load and interact with a SQLite DB.
Provides UI for uploading and downloading .sqlite files.
Optionally stores the DB in IndexedDB for persistence.
Optional Backend (Deno):

For syncing or backing up the database.
Could offer cloud storage or user authentication.
🚀 Want a Demo?
Would you like a working example of a PWA that:

Loads a SQLite file in the browser?
Lets you run queries and save changes?
I can generate a minimal HTML + JS example using sql.js to get you started.


You said:

lets say they close their browser or their cache is reset. how can i ensure their data still persists?
Copilot said:
Copilot
Great question! Ensuring data persistence in a PWA, especially when the browser is closed or cache is cleared, is one of the biggest challenges—especially for something like a SQLite database. Here's a breakdown of your options:

🔐 1. Use IndexedDB for Persistent Storage
IndexedDB is the most reliable way to persist data in the browser, even across sessions and browser restarts.
You can store the SQLite database file (as a binary blob) in IndexedDB.
Libraries like sql.js support loading and saving the database to/from IndexedDB.
✅ Pros:

Survives browser restarts.
Works offline.
No need for server-side storage.
⚠️ Cons:

If the user clears site data, it will be deleted.
Not accessible outside the browser (e.g., by native apps).
☁️ 2. Cloud Sync (Optional but Recommended)
To protect against data loss from cache clearing or device reset:

Offer cloud backup using a backend (e.g., Deno server, Supabase, Firebase).
Sync the SQLite file or its contents periodically.
Authenticate users (e.g., via OAuth or email/password) to associate their data.
✅ Pros:

Data is safe even if the device is lost or reset.
Enables multi-device access.
⚠️ Cons:

Requires backend infrastructure.
Adds complexity (auth, sync logic).
🧪 3. File Download as Backup
Let users download their SQLite file manually:

Provide a “Download Backup” button.
Save the current state of the database as a .sqlite file.
✅ Pros:

Simple and transparent.
Gives users control.
⚠️ Cons:

Relies on users remembering to back up.
🧩 Combined Strategy (Recommended)
For a robust PWA:

Use IndexedDB for local persistence.
Offer cloud sync for resilience.
Allow manual download for user-controlled backup.
Would you like a working example of how to:

Store a SQLite DB in IndexedDB?
Load it back on page reload?
Offer a download button?

---

### Support This Developer
* [**GitHub Sponsors**](https://github.com/sponsors/nomadicGopher)
* [**Ko-Fi**](https://ko-fi.com/nomadicGopher)

<details>
  <summary><b>Crypto Currencies</b></summary>
  <ul>
    <li><b>ETH</b>: 0x7531d86D5Dbda398369ec43205F102e79B3c647A</li>
    <li><b>BTC</b>: bc1qtkuzp85vph7y37rqjlznuta293qsay07cgg90s</li>
    <li><b>LTC</b>: ltc1q9pquzquaj6peplygqdrcxxvcnd5fcud7x80lh8</li>
    <li><b>DOGE</b>: DNQ3GHBVEcNpzXNeB7B4sPqd7L1GhUpMg3</li>
    <li><b>SOL</b>: EQ6QwibvKZsazjvQGJk6fsGW4BQSDS1Zs6Dj79HfVvME</li>
  </ul>
</details>
