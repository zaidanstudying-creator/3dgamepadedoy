# QUIZ BATTLE ARENA 3D

**Think Fast. Answer Smart. Win Together.**

QUIZ BATTLE ARENA 3D is a browser-based multiplayer learning game set in a low-poly school arena. Teachers host rooms, while students join with a room code and answer multiple-choice questions by moving to one of four colored platforms.

## Product goals

- Support teachers and students on desktop and mobile browsers.
- Start with rooms for up to 16 players and four-option multiple-choice questions.
- Let teachers manage rooms through an account and dashboard; students can join without personal accounts in the MVP.
- Keep gameplay state, timers, answer validation, and scoring authoritative on the realtime game server.
- Persist durable data while keeping per-frame player movement out of the database.
- Reveal correct answers only after the answer timer ends.

## Planned technology

- Next.js and TypeScript
- React Three Fiber, Three.js, Drei, and Rapier
- Colyseus for realtime multiplayer game state
- Supabase Auth and PostgreSQL for accounts and persistent data
- Tailwind CSS

## MVP gameplay loop

1. A teacher creates a room and shares its code.
2. Students join, choose a display name and avatar, and enter the arena.
3. The teacher starts the game; all players receive the same question and timer.
4. Players move to answer platform A, B, C, or D.
5. The server accepts at most one locked answer per player, then reveals the answer and calculates scores when time expires.
6. The game continues through the question set, saves the results, and displays a winners' podium.

## Answer platforms and scoring

- A: red
- B: blue
- C: yellow
- D: green
- Correct answer: 1,000 base points plus up to 500 speed bonus
- Incorrect or unanswered: 0 points

## Development status

This repository currently contains the product brief only. Implementation has not started. Development should proceed in approved phases, beginning with a repository and architecture setup review before adding application code.
