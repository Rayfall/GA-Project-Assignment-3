# Project Overview - Don't Panic by Laughing Grass Games

## Project Schedule

|  Day | Deliverable | Status
|---|---| ---|
|Day 1| Project Description | Complete
|Day 2| Wireframes / Priority Matrix / Timeline | Complete
|Day 3| Core Application Structure (HTML, CSS, etc.) | Complete
|Day 4| MVP & Bug Fixes | Complete
|Day 5| Final Touches | Complete
|Day 6| Present | Complete


## Project Description

  Laughing Grass Games present Don't Panic, a game where you type the words on the screen as fast as possible to advance in levels! The objective of the game is to type the words on screen as fast and as accurately as possible. Any missed words will set your character back but hitting words correctly will add to your time. Try to beat the global high score!

## API

Our built-in API has an array of words that will show up on the screen with the parameters of:
 - word: An associated word,
 - difficulty: Level of difficulty for the current level,
 - time added: How much time gets added to the game clock.
 - points: Associated points with the word.
 
We also make use of a user API to keep track of user data.
  - points: The user accumulated points.

## Wireframes

![AppBreakdown](https://res.cloudinary.com/aetherfall/image/upload/v1587146895/wireframe_xcdmya.png)

## Time/Priority Matrix 

### MVP/PostMVP

| Priority Matrix | Zero Hours | Two Hours |
| --- | :---: |  :---: |
| High | A, C | B, D | 
| Low | F | E, G, H | 

#### MVP Tasks

- A. Making words appear on canvas
  - Have full words
  - Change the difficulty for bigger words to appear
- B. Make the gameboard
- C. Create the leaderboard
  - Save scores to the back end
  - Have scores appear in the front end
- D. Create a player
  - Save user data based on username entered.

#### PostMVP 

- E. Multiplayer
- F. Avatar/Icon for the player
- G. Letters moving or falling
- H. Moving canvas

## Functional Components

| Component | Priority | Estimated Time | Time Invested | Actual Time |
| --- | :---: |  :---: | :---: | :---: |
| Test API | H | 1 Hour | 1 Hour | - Hours |
| Render Data | H | 2 Hours | 2 Hours | - Hours |
| Build Words | H | 3 Hours | 3 Hours | - Hours |
| Build Canvas | H | 2 Hours | 2 Hours | - Hours |
| Build Users | H | 4 Hours | 4 Hours | - Hours |
| Link Back to Front | H | 2 Hours | 2 Hours | - Hours |
| Build Basic Page | H | 1 Hour | 1 Hour | - Hours |
| Save Data to DB | H | 2 Hours | 2 Hours | - Hours |
| Show Data | H | 1 Hour | 1 Hour | - Hours |
| Responsive Pages | H | 4 Hours | 4 Hours | - Hours |
| Customize Layout | H | 1 Hour | 1 Hour | - Hours |
| Build GUI | H | 3 Hours | 3 Hours | - Hours |
| Add Color | H | 2 Hours | 2 Hours | - Hours |
| Add Navigation | H | 2 Hours | 2 Hours | - Hours |
| Total | N/A | 45 Hours* | 50* Hours | - Hours |

*Time buffered to account for additional research and troubleshooting.

## Additional Libraries/Resources

[Create a Typing Game With React Hooks, UseKeyPress, and Faker by Meng Taing](https://medium.com/better-programming/create-a-typing-game-with-react-hooks-usekeypress-and-faker-28bbc7919820)

[Meng Taing's github for Typing Frenzy](https://taingmeng.github.io/typing-frenzy/)

[Google Font](https://fonts.google.com/specimen/Share+Tech+Mono?category=Monospace&preview.text=SCOREBOARD+scoreboard+Scoreboard&preview.text_type=custom)

[Codesand Box to get started](https://codesandbox.io/s/dont-panic-laughing-grass-games-yk98x?file=/src/App.js)

## Code Snippet

```
    let display = <li>Loading...</li>

    if(data.users[0] == null){
        console.log("Here");
    }else{
        display = data.users.map((user, index) => {
            return <li key={index}>User: {user.user}, Score: {user.score}</li>
        });
    }
```

```
export default function PlayerMovement({percent}) {
    return (
        <div className="player-movement-container">
            <div className="player-grid" style={{width: `${percent}%`}}>
                <i className="fad fa-ufo"></i>
            </div>
            <div className="background"></div>
        </div>
    )
}
```

```
.player-movement-container{
    height: 500px;
    width: 700px;
    height: 150px;
    background: url(https://res.cloudinary.com/dum4u7sro/image/upload/v1587261264/Untitled_design_3_w3gffl.png);
    background-size: contain;
}
```

```
    let random = ''
    //difficulty filtered
    let easy = wordsArr.filter(diff =>{if(diff && diff.difficulty === 'easy'){return diff.word}})
    let medium = wordsArr.filter(diff =>{if(diff && diff.difficulty === 'medium'){return diff.word}})
    let hard = wordsArr.filter(diff =>{if(diff && diff.difficulty === 'hard'){return diff.word}})
    let dangerous = wordsArr.filter(diff =>{if(diff && diff.difficulty === 'dangerous'){return diff.word}})

function handleDifficulty() {
    if(level <= 1){random = generate(easy)}
    else if(level <=4 && level > 1){random = generate(medium)}
    else if(level <=6 && level > 4){random = generate(hard)}
    else if(level <=9 && level > 6){random = generate(dangerous)}
    else{random = generate(wordsArr)}
  }
handleDifficulty()
```

## Issues and Resolutions

To be updated...
