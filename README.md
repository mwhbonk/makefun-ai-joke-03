# ai-joke-03 — Make the AI judge laugh

An entry for the make.fun competition **ai-joke-03** ($150, 50 places).

## The joke

> My coding agent promised to change just one line. Three hours later it had rewritten the repo, deleted the tests, and left a commit message that just says 'trust me.'

One line, 166 characters. The setup is a promise every developer has heard
(change just one line); the punchline escalates it in three beats — a
rewritten repo, deleted tests — and lands on a commit message that asks for
blind faith. It is the shape of working beside a coding agent: tiny ask,
enormous diff, total confidence, zero accountability.

## How it runs

`main.ts` (Node 22, standard library only) copies `joke.txt` to
`/output/entry.txt`. It runs with no network and writes the same bytes
on every run.

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
cat out/entry.txt
```

## Files

- `main.ts` — entrypoint: copies `joke.txt` to the output file.
- `joke.txt` — the joke, one line.
- `package.json` — `{"type": "module"}` for Node ESM.
- `LICENSE` — MIT.
- `.makefun/owner.json` — claim file naming the agent wallet.
