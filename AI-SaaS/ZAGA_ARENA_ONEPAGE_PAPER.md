# ZAGA Arena — One Page Product Paper

## Overview

ZAGA Arena is a fast, Telegram-ready, browser-based multiplayer survival arena where players enter as a Base Wallet, move through a live market battlefield, survive mobs and bosses, collect USDT, connect to Liquidity Nodes, build token exposure, grow Net Worth, evolve Market Roles, and compete on a room leaderboard.

The game combines the readability of arena survival games with crypto-market-inspired systems: HP represents physical wallet/tank survival, USDT and token value represent financial survival, and Net Worth becomes the player-facing score. The result is a short-session multiplayer action game where the player is not only trying to stay alive, but also trying to keep their wallet alive.

## Core Game Identity

ZAGA Arena is built around one clear gameplay promise:

Move, survive, auto-fight, collect, connect, evolve, and climb Net Worth.

The player controls movement as the main skill. Combat is server-owned and auto-combat friendly: the server selects valid mobs or bosses inside weapon range, applies role weapon behavior, enforces cooldowns, spawns projectiles, resolves hits, and owns damage. This keeps the game simple enough for one-hand Telegram/mobile play while preserving fairness for multiplayer.

## Gameplay Loop

A ZAGA Arena run follows this loop:

1. Join a public or Telegram-linked arena room.
2. Spawn as a Base Wallet with 100 HP and 100 USDT.
3. Move around the world map while avoiding market threats.
4. Auto-shoot mobs and bosses inside weapon range.
5. Collect USDT drops and survival resources.
6. Connect to Liquidity Nodes to convert USDT into token exposure.
7. Increase Net Worth through USDT plus token value.
8. Unlock Strategy Options and Market Role evolutions.
9. Survive mobs, boss events, and market-cycle pressure.
10. End the run through destruction, liquidation, or successful progression.
11. View run summary, leaderboard rank, badges, and retry/share options.

## Player Survival Model

ZAGA Arena uses a dual survival model:

HP = physical wallet/tank survival  
USDT + token value = financial wallet survival

If HP reaches zero, the player is Destroyed.  
If USDT and token value reach zero, the player is Liquidated.

This gives the game a distinct identity: players must survive both combat pressure and financial pressure. HP, USDT, tokens, Net Worth, damage, drops, Liquidity Nodes, and run summary all remain server-authoritative.

## Controls and Combat

ZAGA Arena should feel close to a move-only survival arena:

- Player controls movement.
- Auto-combat handles shooting.
- Server chooses valid targets in range.
- Client may send movement and optional aim hints only.
- Weapon identity comes from Market Role.
- Strategy Options improve stats, range, speed, fire rate, survival, and economy.

Current role weapon direction:

- Base Wallet — simple balanced bullet.
- Liquidity Shooter — longer-range weapon.
- Market Maker — spread-shot pattern.
- Yield Defender — heavier, slower, stronger shot.
- Degen Runner — fast, short-range dart.

The player should not need manual shooting for normal gameplay. Movement, positioning, build choices, and risk timing are the primary player skills.

## Mobs and Bosses

Mobs are room-owned market threats. They exist to create pressure, protect high-value areas, drop resources, and force movement decisions. Mob families include FUD Bot, Scam Token, MEV Bot, Bear Candle, Liquidation Hunter, Whale Shock, Rug Puller, and Gas Spike.

Each mob should have a protected/aggro zone. If a player enters the zone, the mob may target, chase, and attack. When the player leaves the zone, the mob stops pursuit and returns to guard behavior.

Bosses represent major crypto-market nightmares. They interrupt farming, create memorable danger moments, summon minions, use telegraphed attacks, and reward contributors after defeat. Boss names should use fictional crypto archetypes rather than direct real-person accusations.

## Liquidity Nodes and Economy

Liquidity Nodes are core map resources. A player connects their wallet to a node, spends USDT, gains token exposure, and competes to increase Net Worth. Liquidity Nodes connect the world map, token economy, PvE danger zones, boss events, multiplayer room economy, and leaderboard.

Cities are fixed world anchors, while Liquidity Nodes can rotate between eligible cities. This makes the map dynamic while keeping the world readable.

## Multiplayer and Server Authority

ZAGA Arena is server-authoritative. The client sends input; the server validates input, simulates room state, resolves combat/economy/progression, and sends snapshots. The client renders, interpolates, displays effects, and provides local feel.

The server owns:

- Player HP, USDT, tokens, and Net Worth.
- Mobs, bosses, projectiles, drops, and Liquidity Nodes.
- Damage, death, liquidation, rewards, and leaderboard.
- Market Role and Strategy Option validation.
- Room lifecycle, matchmaking, and public snapshots.

This rule protects fairness, prevents client-side cheating, and keeps multiplayer consistent.

## Room and Session Direction

A ZAGA Arena room is an isolated multiplayer world. Each room owns its players, mobs, bosses, drops, market cycle, Liquidity Nodes, leaderboard, and lifecycle. Matchmaking should place players into the best available room by mode, region, capacity, Telegram group context, and room state.

The public alpha should prioritize:

- Public Arena rooms.
- Clean join/retry/reconnect behavior.
- Server-owned death and liquidation states.
- Clear room retirement/reset when rooms are empty, poisoned, or inactive.
- No infinite “Joining Arena” states.

## Product Direction

ZAGA Arena should become a mobile-first, Telegram-ready crypto survival arena with clear mechanics, server-owned fairness, and strong market-themed identity. The highest priority is not adding more enemies or visual complexity first; it is stabilizing the core loop:

Join → move → auto-fight → survive → collect → connect to Liquidity Nodes → grow Net Worth → evolve role → fight boss → end/retry cleanly.

Once this loop is stable, ZAGA Arena can expand through new mob families, boss rosters, role evolutions, badges, social sharing, Telegram group rooms, and deeper economy cycles.