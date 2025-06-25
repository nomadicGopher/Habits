> [!IMPORTANT]
> Habits is in a pre-alpha state, and only suitable for use by developers.
> 
> **Progress to MVP**  
> ░░░░░░░░░░ (0%) <!--█-->

<!--[**Kanban Board**]()--> <!-- TODO: Copy GitHub project (LiberaDebt) & replace. -->

### Tech Stack
* Typescript / JavaScript
  * [Deno 2](https://github.com/denoland/deno?tab=readme-ov-file)
* HTML
* CSS
* [IndexedDB](https://github.com/w3c/IndexedDB) to store the binary blob of a [SQLite](https://github.com/sqlite/sqlite) database file
  * [sql.js](https://github.com/sql-js/sql.js) support loading and saving the database (to & from)
  * **Pros**
    * _Survives browser restarts_
    * _Works offline_
    * _No need for server-side storage_
  * **Cons**
    * If the user clears site data, it will be deleted
    * Not accessible outside the browser (e.g., by native apps)

### To Do
* [ ] Store a SQLite DB in IndexedDB
* [ ] Load it back on page reload
* [ ] Offer a download backup
* [ ] Offer to restore from backup
  * File input `<input type="file">` to let users upload a .sqlite file

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
