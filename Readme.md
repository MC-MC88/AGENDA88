<div align="center">

📅 agenda88

Un calendrier qui vous ressemble, pas à votre boîte mail.

</div>

---

👋 Welcome

I've tried a dozen calendar apps. Every single one of them wanted to be my assistant. They wanted to sync with my email, invite my colleagues, schedule my "focus blocks", send me a notification at 6 AM asking if I'd really like to push that meeting. Somewhere between the first release of Google Calendar and whatever Notion shipped last Tuesday, "calendar" stopped meaning "a place to write down what I'm doing" and started meaning "another app that manages my life for me."

agenda88 doesn't do any of that.

It's a calendar that lives in a single HTML file. You open it, you see a month, you tap a day, you write something down. That's the whole relationship. Your events stay in your browser's local storage — no account, no sync, no cloud, no team workspace, no "Upgrade to Pro to unlock recurring events." Just a calendar, ten color themes, and a background photograph that changes every time you open the page.

It's the calendar you'd build for yourself if you'd had enough of everyone else's.

The design leans warm and playful — thick borders, chunky rounded corners, a hand-lettered font for the title, buttons that lift when you hover and press when you click. Ten themes sit behind a single toggle button: Cream, Midnight, Sepia, Ocean, Forest, Sunset, Lavender, Mono, Blossom, Neon. Each one changes the fonts, the corners, the shadows, the colors — not just a tint on the same layout. Switching feels like stepping into a different room.

---

<!--
## 📸 Look Inside

<br />

<div align="center">
  <img src="https://github.com/mohamed005cheikh-rgb/agenda88/raw/main/images/preview-1.png" alt="The month grid in the Cream theme" width="100%" />
  <br />
  <sub><b>① The month grid</b></sub>
</div>

<br />
<br />

<div align="center">
  <img src="https://github.com/mohamed005cheikh-rgb/agenda88/raw/main/images/preview-2.png" alt="Adding an event" width="100%" />
  <br />
  <sub><b>② Adding an event</b></sub>
</div>

<br />
<br />

<div align="center">
  <img src="https://github.com/mohamed005cheikh-rgb/agenda88/raw/main/images/preview-3.png" alt="The Neon theme" width="100%" />
  <br />
  <sub><b>③ The Neon theme</b></sub>
</div>
-->

---

✨ What you'll find

A month, drawn plainly.
Seven columns, one row of weekday headers, a grid of numbered days. Today is highlighted and gently pulses so you always know where you are. Days that hold events carry a small dot underneath the number — one glance and you can see the shape of your month without opening a single entry.

Add an event in three taps.
Click a day. The modal opens with the date in the header, a title field, a description field, and a Save button. Type the title, tap Save, done. The event appears below the form, immediately, alongside anything else you've added to that day.

See everything scheduled for a day, at once.
When you open a day, you don't just see a blank form — you see the list of what's already there. Each entry sits on its own row with a colored bar on the left. Delete one with a single click, and the day updates instantly, both inside the modal and back on the grid.

Ten themes, one button.
The circular toggle in the top-right corner cycles through every theme. Cream is warm and orange. Midnight turns the whole thing purple on near-black. Sepia uses a handwritten font on parchment. Ocean, Forest, Sunset carry their mood into the borders and shadows. Lavender softens everything into round pastels. Mono strips color entirely — square corners, black borders, no decoration. Blossom is pink and cheerful. Neon glows. Your choice is remembered the next time you open the file.

A background that changes every visit.
Every time the page loads, agenda88 fetches a fresh random photograph from Picsum and lays it behind the calendar. The panel floats on top with a soft blur, and a themed overlay keeps the text readable whatever the photo throws at it. Same calendar, different scenery, every morning.

Events that survive refreshes.
Everything you write is saved to your browser's localStorage the moment you hit Save. Close the tab, reopen the file tomorrow, and your month is exactly where you left it — events, descriptions, everything.

Two directions, and then some.
The arrow buttons step you forward and backward through the months. Nothing is capped. You can scroll back to last year to see what you did, or skip ahead to next spring to plan a trip — the events you've already written stay attached to their days.

---

🧭 How it works

1. Open the file.
One HTML file, no build step, no server. Double-click it and the calendar appears with the current month already in view. Your saved theme loads automatically — or Cream if it's your first time.

2. Pick a day.
Click any numbered cell. The modal opens with that date in the header and any events you've already added to it listed below.

3. Write something down.
Give the event a title — that's the only required field. Add a description if you want one. Press Save Event. It appears in the list immediately, and a dot appears on the day back in the grid.

4. Move around the year.
Use the arrows in the calendar header to go back and forward by month. Your events travel with their dates, and the dot markers stay attached to the right days.

5. Delete what you don't need.
Each event in the list has a small red ✕ on the right. Click it and the event disappears, from both the day's list and the grid. No confirmation, no undo — but it's also gone the second you wanted it gone.

6. Change the mood.
Click the round button next to the title. The entire interface — fonts, colors, corners, shadows — shifts to the next theme. Click again for the one after. Ten themes in a loop, and the last one you chose is the one you'll see next time.

That's the whole app. There is no settings menu, no account page, no export button, no premium tier. It's a calendar and a paint set.

---

🛠️ A few small helps

"Where is my data stored?"
Entirely in your browser's localStorage, on your own device. Nothing is uploaded, nothing is synced. If you clear your browser data — or open the file on a different device — the events won't follow you. For a calendar that lives in one place, that's the point.

"Can I use it on my phone?"
Yes. The layout is fully responsive and the day cells shrink gracefully on small screens. The theme toggle and the arrows both have touch-specific handling so they respond the instant your finger lands, without the usual 300 ms delay.

"Why does the background change every time I open it?"
Every load fetches a new random photograph from Picsum, a free public image service. It's decorative — nothing is uploaded, and the calendar works perfectly without an internet connection (the photo will simply not appear). If you'd rather have a static background, you can replace the setBackground() function with a hard-coded URL.

"One of my events disappeared."
Two possibilities. Either the browser cleared its local storage — some browsers clear it after long periods of inactivity, or when you're in private browsing — or you deleted it and forgot. There's no undo and no history, so treat it like a paper calendar: write down anything you can't afford to lose somewhere else too.

"The theme doesn't stick between visits."
If you're in private browsing mode, localStorage is disabled and nothing persists. Open the file in a normal window and both your events and your chosen theme will be remembered.

"Can I have more than one event on the same day?"
Yes, as many as you want. They stack in the list inside the modal, oldest at the top, and the day cell shows a single dot regardless of how many events it holds. The dot means there's something here, not how much.

"What about recurring events?"
Not built in. If you have a weekly meeting, add it to each day individually. That's the honest answer. Adding recurrence would mean a rules engine, an editor for it, exception handling, and a settings menu — and the moment that exists, agenda88 stops being a calendar you open and starts being a calendar that manages you.

"Can I print the month?"
Not as a feature, but it prints fine — the grid, the numbers, the dots all render on a standard print. The background photo and the modal won't appear, which is probably what you want anyway.

"Does it work offline?"
The calendar itself, yes — everything is one file, no external dependencies except the fonts and the background image. If you're offline, the fonts fall back to system defaults and the background goes blank. The calendar, your events, and the theme toggle all keep working.

"How do I change the theme without clicking?"
You can't — the toggle is the only way. There's no keyboard shortcut, no settings page. If you want one specific theme permanently, open the file in a text editor and change data-theme="cream" on the <html> tag at the top to whichever theme you prefer. It'll stay there.

---

<div align="center">

📞 A question, an idea, a bug?

https://img.shields.io/badge/Email-mohamed005cheikh@gmail.com-d14836?style=flat-square&logo=gmail&logoColor=white
https://img.shields.io/badge/WhatsApp-+222_30_73_64_75-25D366?style=flat-square&logo=whatsapp&logoColor=white
https://img.shields.io/badge/GitHub-mohamed005cheikh--rgb-181717?style=flat-square&logo=github

<br />

Your days. Your colors. No accounts.

<sub>© 2026 Mohamed Cheikh — MC88</sub>

</div>
