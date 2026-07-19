# F8WC Final Risk'em

This package updates the app for the World Cup Final:

- Spain vs Argentina
- Single locked $400 team pick
- Team odds to lift the Cup: Spain -156 / Argentina +136
- Final score prediction
- Shootout prop: Yes / No
- Golden Boot prop: Messi / Tie / Mbappé
- Entry export by copy/text/email/CSV
- Scoreboard with optional commissioner CSV import using `scoreboard.html?commissioner=1`

## Scoring

Starting budget is $400.

Team pick:
- Correct champion: odds profit on the locked $400 wager
- Wrong champion: -$400

Score bonus, only if champion pick is correct:
- Exact score: +$100
- Correct margin: +$50
- Correct total goals: +$25
- One team score exact: +$15

Props:
- Golden Boot: +$100
- Shootout exact: +$50

Final score is after extra time, before penalty shootout kicks.


## Golden Boot note

The final prop is labeled **Golden Boot** in the app. CSV import also accepts older exports that used the header `Golden Boot`.


## Visual update

- Team-color kit cards added for Spain and Argentina.
- Spain uses red/yellow kit styling.
- Argentina uses sky-blue/white striped kit styling.
- Bam Bam's submitted card and Mongoose's submitted card are included in `scoreboard.html`.


## Seeded final entries

Included in `scoreboard.html`:

- Bam Bam: Spain 2-1 Argentina, Spain -156, Golden Boot Mbappé, Shootout No.
- Mongoose: Argentina 2-1 over Spain, Argentina +136, Golden Boot Messi, Shootout No.

- K9Beach: Argentina 3-1 over Spain, Argentina +136, Golden Boot Tie, Shootout No.


## Locked picks reveal

`scoreboard.html` now has `REVEAL_LOCKED_PICKS = true`, so public users can see all submitted cards.


## Live API test mode

`scoreboard.html` now includes a browser-side ESPN live API test panel.

- Test Live API: fetches the ESPN FIFA World Cup scoreboard.
- Apply API Score Locally: applies Spain/Argentina score and winner in this browser only.
- Clear Local API Result: removes the browser override and returns to the manual scoreboard state.
- Golden Boot and Shootout can still be set manually in the test panel before applying.
- Live in-progress scoring is labeled as `Live Test`; final props do not score during live preview mode.


## Spain 1-0 final state

`scoreboard.html` is set to:

```js
complete: true
aScore: 1
bScore: 0
winner: "Spain"
shootout: "No"
goldenBoot: "Mbappé"
```

Golden Boot final:
- Kylian Mbappé — 10 goals, 4 assists
- Lionel Messi — 8 goals, 4 assists
- Jude Bellingham — 7 goals, 1 assist
- Erling Haaland — 7 goals
