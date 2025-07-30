---
layout: post
category: coding
subtitle: Taking My Own Advice
---

Since my first [State of the Engine post]({{ site.baseurl }}{% link _posts/2024-10-16-state-of-the-engine.md %}), I wrote about some strategies for prioritizing what you work on as you develop your game. Given it's been about a year since that post, I was curious to see how much progress had been made and if I actually did what I preached. I know I am prone to getting distracted by engine related changes but I have been trying to only do them if they would make implementing other game features more efficient.

Let's start with some updated metrics, deltas since the last post are in brackets:

- **29961** lines of code (+5239)
- **3660** comments (+765)
- **445** todos (+66)
- **18608** lines of JSON data (+12682)

I am always looking to make my game as data driven as possible ever since I read the first chapter of [Game Programming Gems](https://www.goodreads.com/book/show/318957.Game_Programming_Gems) back in college. So I am really glad to see the JSON data metric skyrocket but I know for a fact I did not write 12000 lines of JSON by hand. Upon further investigation, I realized the game's map file had increased the most. I know that JSON is not the best format for a map file and it most likely will change prior to release but let's not solve problems until they actually exist.

The code increase is larger than I thought it would be so that's good progress. The comments and todos are hinting at gradual tech debt accumulating and partial feature implementation. It's progress over perfection right now but I will eventually have to come back and address that.

---

But metrics aside, what has actually changed since then?

I ran this at my terminal to see what I've worked on:

```
git log --since='Oct 31, 2024' --pretty=format:'%C(blue)%ad:%Creset %s' --date=short
```

And then came up with this list:

- Fences and torches
- Started the Wizard NPC
- First spell in the game (it’s a secret)
- Warp areas to connect map areas and triggers that can fire off cutscenes
- Added the ability to place entities in the map editor (fences, doors, other objects)
- Added UTF-8 support
- Updated the game's bitmap font to support EFIGS [^1], Portuguese, Polish and Turkish
- Items, cutscenes and dialogue are translatable (they use string keys instead of hardcoded English values)
- Multiline support for text
- Quests and the Quest Journal
- Crafting Screen and Crafting Recipes
- Loot Tables

---

It’s honestly been good to reflect. I feel like for the last six months I had been running out of steam and the game was just sitting on the backburner but overall progress is clearly still being made.

I’m also starting to slowly run out of core systems to implement. NPCs, their schedules, dialogue trees, inventory management, a few physics/collision tweaks and mostly cutscene related functionality needs to be added but it feels like there’s an end in sight. Gameplay is becoming the bigger focus and engine changes are being driven by that which is the balance I want at the moment.

I am really looking forward to building out the rest of the world now that I can link areas together, create quests and interact with objects. It's slowly starting to feel like an actual game. I really want to build out the first playable pillar of the game at least in a rough form and then start polishing it to get to a demo-able state.

_Let's see what the next year holds..._

---

[^1]: EFIGS is English, French, Italian, German and Spanish. A common set of languages targetted by software. Portuguese (Brazil) and Russian are also common for reaching a larger audience as well as CJK (Chinese, Japanese, Korean).
