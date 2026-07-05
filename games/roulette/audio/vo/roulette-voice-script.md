# Roulette HOST — Croupier Voice Line Script

Takes per item are **not uniform** — event/flow lines carry the host's personality
and repeat often within a session, so they get **3 distinct takes**. Number and colour
calls are functional result announcements a real croupier keeps consistent, so they get
**2 takes**. One take chosen at random each play.

File each take under the matching manifest path, e.g. `audio/vo/classic/number/17/1.mp3`,
`audio/vo/classic/place_your_bets/2.mp3`.

Line-key → folder reference:

| Key | Folder |
|---|---|
| placeYourBets | `place_your_bets/` |
| noMoreBets | `no_more_bets/` |
| spinning | `spinning/` |
| payingOut | `paying_out/` |
| winningNumber | `winning_number/` |
| winner | `winner/` |
| signoff | `signoff/` |
| col_red / col_black / col_green | `colour/red/` `colour/black/` `colour/green/` |
| num_0 … num_36, num_00 | `number/0/` … `number/36/`, `number/00/` |

Note on delivery: `callWinningNumber()` plays the number line, then the colour line.
So write each number as a bare number (no colour), and let the colour file follow —
e.g. **"Seventeen."** + **"Black."** → "Seventeen. Black." Don't bake the colour into
the number take, or you'll get "Seventeen black. Black."

Event/flow cells are take **1 / 2 / 3**. Number & colour cells are take **1 / 2**.

---

## CLASSIC — measured, traditional croupier

### Flow & finale (3 takes)

| Key | Take 1 | Take 2 | Take 3 |
|---|---|---|---|
| placeYourBets | Place your bets, please. | Make your bets, ladies and gentlemen. | Let's have your stakes down. |
| noMoreBets | No more bets. | That's no more bets. | Bets are closed. |
| spinning | Round and round she goes. | The wheel is in motion. | And away it spins. |
| payingOut | Paying the winners. | Settling the table. | Winners paid, please. |
| winningNumber | The winning number. | And the result. | We have a result. |
| winner | And that's our champion. | The winner takes the table. | Top of the board — congratulations. |
| signoff | Thank you all for playing. | That's the game, ladies and gentlemen. | Until next time — good night. |

### Colours (2 takes)

| Key | Take 1 | Take 2 |
|---|---|---|
| col_red | Red. | On the red. |
| col_black | Black. | On the black. |
| col_green | Green. | The house pocket — green. |

### Number calls (2 takes)

| Key | Take 1 | Take 2 |
|---|---|---|
| num_0 | Zero. | Zero, the single. |
| num_00 | Double zero. | Double zero. |
| num_1 | One. | Number one. |
| num_2 | Two. | Number two. |
| num_3 | Three. | Number three. |
| num_4 | Four. | Number four. |
| num_5 | Five. | Number five. |
| num_6 | Six. | Number six. |
| num_7 | Seven. | Number seven. |
| num_8 | Eight. | Number eight. |
| num_9 | Nine. | Number nine. |
| num_10 | Ten. | Number ten. |
| num_11 | Eleven. | Number eleven. |
| num_12 | Twelve. | Number twelve. |
| num_13 | Thirteen. | Number thirteen. |
| num_14 | Fourteen. | Number fourteen. |
| num_15 | Fifteen. | Number fifteen. |
| num_16 | Sixteen. | Number sixteen. |
| num_17 | Seventeen. | Number seventeen. |
| num_18 | Eighteen. | Number eighteen. |
| num_19 | Nineteen. | Number nineteen. |
| num_20 | Twenty. | Number twenty. |
| num_21 | Twenty-one. | Number twenty-one. |
| num_22 | Twenty-two. | Number twenty-two. |
| num_23 | Twenty-three. | Number twenty-three. |
| num_24 | Twenty-four. | Number twenty-four. |
| num_25 | Twenty-five. | Number twenty-five. |
| num_26 | Twenty-six. | Number twenty-six. |
| num_27 | Twenty-seven. | Number twenty-seven. |
| num_28 | Twenty-eight. | Number twenty-eight. |
| num_29 | Twenty-nine. | Number twenty-nine. |
| num_30 | Thirty. | Number thirty. |
| num_31 | Thirty-one. | Number thirty-one. |
| num_32 | Thirty-two. | Number thirty-two. |
| num_33 | Thirty-three. | Number thirty-three. |
| num_34 | Thirty-four. | Number thirty-four. |
| num_35 | Thirty-five. | Number thirty-five. |
| num_36 | Thirty-six. | Number thirty-six. |

---

## VEGAS — high-energy showroom host

### Flow & finale (3 takes)

| Key | Take 1 | Take 2 | Take 3 |
|---|---|---|---|
| placeYourBets | Alright, get those bets down! | Money on the felt, let's go! | Place 'em if you've got 'em! |
| noMoreBets | No more bets! | That's it — hands off! | Betting's done, here we go! |
| spinning | And she's spinning! | Round she goes — watch that ball! | Here we go, folks! |
| payingOut | Pay the winners! | Cashing you out! | Winners get paid — yes! |
| winningNumber | And the winner is! | Here's your number! | Check the board, baby! |
| winner | Give it up for our champion! | That's your big winner, baby! | Top of the board — take a bow! |
| signoff | Thanks for playing, you've been great! | That's the game — get home safe! | Catch you next time, high rollers! |

### Colours (2 takes)

| Key | Take 1 | Take 2 |
|---|---|---|
| col_red | Red! | It's red, baby! |
| col_black | Black! | Landing on black! |
| col_green | Green — the house! | Green! Oh, tough one! |

### Number calls (2 takes)

| Key | Take 1 | Take 2 |
|---|---|---|
| num_0 | Zero! | Zero — house number! |
| num_00 | Double zero! | Double zero, folks! |
| num_1 | One! | Number one! |
| num_2 | Two! | Number two! |
| num_3 | Three! | Number three! |
| num_4 | Four! | Number four! |
| num_5 | Five! | Number five! |
| num_6 | Six! | Number six! |
| num_7 | Lucky seven! | Seven, baby! |
| num_8 | Eight! | Number eight! |
| num_9 | Nine! | Number nine! |
| num_10 | Ten! | Number ten! |
| num_11 | Eleven! | Number eleven! |
| num_12 | Twelve! | Number twelve! |
| num_13 | Thirteen! | Unlucky thirteen! |
| num_14 | Fourteen! | Number fourteen! |
| num_15 | Fifteen! | Number fifteen! |
| num_16 | Sixteen! | Number sixteen! |
| num_17 | Seventeen! | Number seventeen! |
| num_18 | Eighteen! | Number eighteen! |
| num_19 | Nineteen! | Number nineteen! |
| num_20 | Twenty! | Number twenty! |
| num_21 | Twenty-one! | Number twenty-one! |
| num_22 | Twenty-two! | Number twenty-two! |
| num_23 | Twenty-three! | Number twenty-three! |
| num_24 | Twenty-four! | Number twenty-four! |
| num_25 | Twenty-five! | Number twenty-five! |
| num_26 | Twenty-six! | Number twenty-six! |
| num_27 | Twenty-seven! | Number twenty-seven! |
| num_28 | Twenty-eight! | Number twenty-eight! |
| num_29 | Twenty-nine! | Number twenty-nine! |
| num_30 | Thirty! | Number thirty! |
| num_31 | Thirty-one! | Number thirty-one! |
| num_32 | Thirty-two! | Number thirty-two! |
| num_33 | Thirty-three! | Number thirty-three! |
| num_34 | Thirty-four! | Number thirty-four! |
| num_35 | Thirty-five! | Number thirty-five! |
| num_36 | Thirty-six! | Number thirty-six! |

---

## SMOOTH — laid-back lounge dealer

### Flow & finale (3 takes)

| Key | Take 1 | Take 2 | Take 3 |
|---|---|---|---|
| placeYourBets | Whenever you're ready — bets down. | Let's see those chips. | Take your time, place your bets. |
| noMoreBets | That's no more bets. | All done betting. | We're locked in. |
| spinning | Here she goes. | Let the wheel do its thing. | Sit back — she's spinning. |
| payingOut | Paying you out. | Let's settle up. | Winners, come get it. |
| winningNumber | And here's your number. | Let's see where she landed. | There it is. |
| winner | And there's your winner. | Top of the table — well played. | That's the one to beat. Congrats. |
| signoff | Thanks for hanging out. | That's the game, folks. | Catch you next time. |

### Colours (2 takes)

| Key | Take 1 | Take 2 |
|---|---|---|
| col_red | Red. | On the red. |
| col_black | Black. | Landed on black. |
| col_green | Green. That's the house. | Green — tough break. |

### Number calls (2 takes)

| Key | Take 1 | Take 2 |
|---|---|---|
| num_0 | Zero. | Zero, the single. |
| num_00 | Double zero. | Double zero. |
| num_1 | One. | Number one. |
| num_2 | Two. | Number two. |
| num_3 | Three. | Number three. |
| num_4 | Four. | Number four. |
| num_5 | Five. | Number five. |
| num_6 | Six. | Number six. |
| num_7 | Lucky seven. | Number seven. |
| num_8 | Eight. | Number eight. |
| num_9 | Nine. | Number nine. |
| num_10 | Ten. | Number ten. |
| num_11 | Eleven. | Number eleven. |
| num_12 | Twelve. | Number twelve. |
| num_13 | Thirteen. | Number thirteen. |
| num_14 | Fourteen. | Number fourteen. |
| num_15 | Fifteen. | Number fifteen. |
| num_16 | Sixteen. | Number sixteen. |
| num_17 | Seventeen. | Number seventeen. |
| num_18 | Eighteen. | Number eighteen. |
| num_19 | Nineteen. | Number nineteen. |
| num_20 | Twenty. | Number twenty. |
| num_21 | Twenty-one. | Number twenty-one. |
| num_22 | Twenty-two. | Number twenty-two. |
| num_23 | Twenty-three. | Number twenty-three. |
| num_24 | Twenty-four. | Number twenty-four. |
| num_25 | Twenty-five. | Number twenty-five. |
| num_26 | Twenty-six. | Number twenty-six. |
| num_27 | Twenty-seven. | Number twenty-seven. |
| num_28 | Twenty-eight. | Number twenty-eight. |
| num_29 | Twenty-nine. | Number twenty-nine. |
| num_30 | Thirty. | Number thirty. |
| num_31 | Thirty-one. | Number thirty-one. |
| num_32 | Thirty-two. | Number thirty-two. |
| num_33 | Thirty-three. | Number thirty-three. |
| num_34 | Thirty-four. | Number thirty-four. |
| num_35 | Thirty-five. | Number thirty-five. |
| num_36 | Thirty-six. | Number thirty-six. |
