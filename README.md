[# sumo-](https://benson0929.github.io/sumo-/index.html)

SUMO | Final Project Proposal
1. Project Proposal
SUMO is a 3D fighting game where the goal is to knock your opponent off the platform. Players move, attack, defend, and recover to the platform. The current version supports matches against a computer opponent. For the final project, I plan to add online two-player matches, allowing players to compete from separate computers.

The platform is carried by a group of people. It tilts in response to the fighters’ positions and heavy attacks. When pressure builds up at a corner, that corner temporarily collapses. Players must watch their opponent, their own position, and the changing platform to find opportunities to attack.

Building on the current web version, I plan to add online multiplayer and refine the character animations, combat feedback, and platform interactions. I want players to feel the weight of each attack, the danger of losing their balance, and the satisfaction of launching an opponent off the platform.

Target Audience

Computer users who enjoy fast-paced action games and competing with friends, including players who are new to this type of game.

Core Experience
1. One player creates a room, and the other joins from another computer.
2. Both players select their characters and review the controls.
3. They fight, landing attacks to build up their opponent’s damage gauge.
4. They respond to their opponent’s actions and the platform’s tilt, trying to launch their opponent while avoiding being knocked out.
5. The first player to win two rounds wins the match.
2. Scope and Plan
Must
- Add online two-player matches with room creation, joining, and control instructions.
- Synchronize player actions, combat results, platform changes, and scores.
- Preserve the core combat mechanics, platform tilting, and corner collapse.
- Improve character animations, hit feedback, and the readability of platform changes.
- Adjust the camera and interface so both players can identify their characters, damage gauges, and scores.
- Complete the match flow: first to win two rounds, results, and restart.
Should
- Add characters or stages.
- Add extra sound effects and transition sequences.
Nice
- Test and refine PlayStation controller support.
- Add match settings, such as the number of rounds needed to win.
Stopping Point

Two players on separate computers can reliably complete an online match in the existing stage, with consistent combat results, clear feedback, and the same final score.

Possible Cut

If time is limited, drop the additional stage and prioritize online multiplayer and the core experience.

Components and Data
Component	Main Data
Connection and rooms	Room code, player IDs, connection status
Player input	Movement direction, button inputs
Character combat	Position, actions, damage, hit states
Platform response	Tilt angles, corner pressure, recovery time
Match flow	Round state, scores, winner


Tools and Resources

Use HTML, JavaScript, Three.js, and the existing models, animations, and materials. Manage the source code through GitHub and host the frontend on GitHub Pages. Test a separately hosted WebSocket server for communication and shared game state.

3. Small Experiment: Online Multiplayer Synchronization
Question

Can two players on separate computers see consistent movement and hit results during a short online interaction?

Prediction

I expect basic movement and one attack to synchronize between both computers, but network delay may affect how responsive the interaction feels.

Setup
1. Build a small networking prototype with two simple characters and one basic attack.
2. Connect two computers on separate networks to the same room.
3. Have both players move simultaneously, then take turns attacking.
4. Check whether both screens agree on character positions, successful hits, and damage.
5. Record both screens and note visible delays or disagreements.
Actual Result

Pending. No measured result has been recorded yet.

Next Decision

If movement and hit results remain consistent, continue integrating the networking approach into SUMO. If the screens disagree or controls feel too delayed, revise the synchronization approach before adding more combat features.

Remaining Uncertainty

This test will not yet establish how well the connection handles the full game’s platform physics, complex combat, or slower and unstable internet connections.
