[# sumo-](https://benson0929.github.io/sumo-/index.html)

SUMO | Final Project Proposal
1. Project Proposal
SUMO is a 3D fighting game where the goal is to knock your opponent off the platform. Players move, attack, defend, and try to recover when they are launched off. The current build is a single-player game against a computer opponent. For the final project, I want to add online matches between two players on separate computers.

The platform is carried by a group of people. It tilts with the fighters’ positions and heavy attacks, and a corner can temporarily collapse when enough pressure builds up. This makes positioning part of the fight: players have to watch both their opponent and the ground beneath them.

Alongside online play, I want to improve the character animations, hit feedback, and platform reactions. My aim is to make attacks feel heavy and give players a clear sense of when they are in danger of being knocked out.

Target Audience

People who enjoy fast-paced action games and playing against friends, including newcomers to platform fighting games.

Core Experience
1. One player creates a room, and the other joins from another computer.
2. Both players select their characters and review the controls.
3. They fight, landing attacks to build up their opponent’s damage gauge.
4. They use their position and the platform’s tilt to find openings, launch their opponent, and recover when knocked off.
5. The first player to win two rounds wins the match.
2. Scope and Plan
Must
- Add online two-player matches with room creation, joining, and control instructions.
- Keep player actions, hit results, platform changes, and scores consistent on both computers.
- Preserve the core combat mechanics, platform tilting, and corner collapse.
- Improve character animations, hit feedback, and the visibility of platform changes.
- Make characters, damage gauges, and scores easy to identify on both screens.
- Complete the match flow, including results and restarting.
Should
- Add characters or stages.
- Add extra sound effects and transition sequences.
Nice
- Test and refine PlayStation controller support.
- Add match settings, such as the number of rounds needed to win.
Stopping Point

Two players on separate computers can join the same room and complete a match in the existing stage. Both screens show consistent combat results and the same final score.

Possible Cut

If time is limited, I will drop the additional stage and focus on online play and the existing combat experience.

Components and Data
Component	Main Data
Connection and rooms	Room code, player IDs, connection status
Player input	Movement direction, button inputs
Character combat	Position, actions, damage, hit states
Platform response	Tilt angles, corner pressure, recovery time
Match flow	Round state, scores, winner


Tools and Resources

The game uses HTML, JavaScript, Three.js, and existing models, animations, and materials. I will use GitHub for the source code and GitHub Pages for the frontend. A separately hosted WebSocket server is the starting approach I plan to test for online play.
3. Small Experiment: Online Synchronization
Question

Can two players on separate computers see consistent movement and hit results during a short online interaction?

Prediction

I expect basic movement and one attack to synchronize, but network delay may make the controls feel less immediate.

Setup
1. Build a small networking prototype with two simple characters and one basic attack.
2. Connect two computers on separate networks to the same room.
3. Have both players move at the same time, then take turns attacking.
4. Compare character positions, successful hits, and damage values on both screens.
5. Record both screens and note visible delays or disagreements.
Actual Result

No test result has been recorded yet. This section will be updated with the first attempt, recordings, and any connection or synchronization problems.

Next Decision

If both screens agree on movement and hit results, I will continue integrating this approach into SUMO. If they disagree or the controls feel too delayed, I will revise the synchronization approach before adding more combat features.

What Remains Uncertain

This small test will not establish how the full game handles platform physics, complex combat, or unstable connections.
4. Handoff
Current Build

The proposal baseline is the existing single-player prototype shared as SUMO_project.zip. Online multiplayer is still planned.
- Playable build: SUMO
- Required setup: A computer, keyboard, and browser with WebGL support.
- Tutorial: Available on first launch and through the Tutorial button.
Running the Source Locally

From the supplied project folder, run:
python3 -m http.server 8765

Then open:
http://localhost:8765/sumo.html

Main Controls
Input	Action
WASD	Move
Space	Jump; press again in the air for the rising special
J	Attack
L	Heavy attack; hold to charge
K	Roll
I	Parry
Esc	Pause
R	Restart


Roles and Support

I am responsible for the project’s design direction and integration. The online test will need a second person using another computer on a separate network. We will compare both screens and record connection issues and differences in the match state.

AI and Source Credits

I am developing SUMO with Claude Code, which helps me write and revise the game code. I make the game design decisions and guide the development, including the mechanics, visual direction, and player experience.

ChatGPT helped review the project code and organize this proposal and experiment plan.

Asset attributions are included in CREDITS.md, and the tatami texture license is included in assets/tatami/LICENSE.txt. These files should stay with the project source.

Initial Privacy and Accessibility Check

The current controls do not require a camera or microphone. For the online prototype, I plan to use room codes without requiring real names or email addresses. Server logging and data retention still need to be checked during implementation.

The game includes English and Traditional Chinese tutorials. It currently relies on quick button inputs and uses camera movement and flashes. I still need to check text readability, character identification, and options for reducing camera shake and flashing effects.
