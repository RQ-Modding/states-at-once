# States at Once

In a fight, a character can be **poisoned and stunned** at once, and have both **▲ and ▼** of one
stat. In the game a new state replaces the old one.

## What it changes

- **Poison and stun together.** Poison still deals its damage on the turn a character only recovers
  from the stun.
- **▲ and ▼ together** cancel each other out.
- **Cures take what they say:** recovering from a stun takes only the stun, First Aid only the
  poison, and a cure of ▼ or a removal of ▲ only its own side. Encourage, Self-Healing and Status
  Restore take both poison and stun. Death takes everything.
- As in the game, a Barrier still blocks poison, a stun still cancels a charge, and no character is
  stunned twice in a row.

## Keys and settings

None.

## Saves

Nothing. The second state is not in the save, and it is forgotten when the fight ends.

## Works with

Mods that read a character's state with `rq.chara.get` see one value per stat, the one that came
first (stun over poison); `rq.battle.states` lists both.

## Install

Needs [RQ MOD](https://github.com/RQ-Modding/RQ-Mod) with loader **0.31.0** or newer. Extract the
release zip into the game's `mods` folder, so that you have `mods/states-at-once/mod.json`.

## How it works

The rules are the engine's, from one call: `rq.battle.install_states()`.

## License

MIT, see [LICENSE](LICENSE).
