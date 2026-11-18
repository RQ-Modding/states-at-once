# Testing States at Once

For people and agents who test the mod in the game. Check `logs\rqmod.log` for
`Loading states-at-once` first.

## What it adds

No buttons and no `rq.agent.control` ids. Do not invent controls for it.

## How to check it

1. In a fight, poison a character, then stun it (Deadly Mist, then Hypnotism; a stun by Hypnotism
   needs `rq.random.fix(1)` from a throwaway test mod). Both marks show, and `rq.battle.states`
   lists both.
2. On the turn the stun ends, the poison still deals its damage.
3. First Aid takes only the poison; Encourage or Status Restore take both.
4. ▲ and ▼ of one stat (Queen's Curse on a buffed character) both show and cancel out.
5. In the next fight neither second state is left.

Without the mod (remove it from the Mods copy), stun replaces poison and ▼ replaces ▲.

## Tested in the game

The Test Lab's scenario `states`: all of the above through real skills, with shots to check by eye.
