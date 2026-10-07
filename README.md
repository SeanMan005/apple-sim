# The Apple Engine

An interactive simulation of an apple tree's growing season. Set the inputs, then watch the tree turn sunlight into sugar, fruit, and seed, or stall partway when the inputs run short.

**Live demo:** https://seanman005.github.io/apple-sim/

## What it shows

The tree runs the same process every season: catch sunlight, turn it into sugar, build fruit, ripen it, and finish the seed. The machine never changes. Only the inputs do. A good season carries the process all the way to a finished seed. A poor one stops partway, producing small, sour, unfinished fruit that looks like a broken machine but is actually a fuel problem.

## Controls

| Parameter | What it changes |
|---|---|
| Sunlight | How much light is available |
| Water | How much water is available |
| Base breadth | Number of leaves and roots. More catches more energy but costs more to maintain |
| Base discipline | How consistently the leaves and roots do their job. Low discipline makes supply uneven |
| Routed to fruit | Share of sugar sent to the fruit instead of kept in reserve |
| Forager traffic | How many animals are around to eat the fruit and carry the seed |

**Presets:** Rich season, Thin season, Wide dull base, Free-form base, All-in on flesh, Hoard the sugar

**Events:** trigger a drought (cuts water 55%) or drop the fruit early to see the cost of abandoning it

## How it works

The model runs day by day over a 180-day season, moving energy up five stages:

1. **Sunlight, water, air** are captured by the leaves
2. **Sugar** is produced and stored
3. **Fruit flesh** is built from sugar routed to it
4. **Ripening** unlocks only once the seed is far enough along
5. **The seed** is the only output that lasts past the season

Live readouts track surplus energy, reserve stress, sweetness, acidity, firmness, and how attractive the fruit is to animals. At the end of each season, a ledger shows what was lost and what survived, and successful seeds start new trees on the ground map.

## Things to try

- **Drop base breadth to 20 with full sunlight.** The light is still there, but the tree can't catch enough, and growth stalls at the fruit stage.
- **Set base breadth to 260, then 520.** Past about 260, more leaves shade each other and cost more upkeep, so the tree ends up with *less* surplus.
- **Pick "Free-form base."** Uneven supply weakens every stage above it.
- **Pick "Thin season," or trigger a drought around day 90.** The same machine stops partway and produces sour fruit.
- **Watch the dispersal signal as the seed finishes.** Half-ripe fruit is only about 6% as attractive as ripe fruit, so animals ignore it until the seed is ready.
- **Drop the fruit on day 30, then on day 150.** Abandoning early costs almost nothing. Abandoning late wastes the whole season.

## Limitations

- This is a conceptual model, not a botanically calibrated one. Values are illustrative, not measured from real trees.
- Weather is simplified to sunlight and water, with no temperature, pests, or soil effects.
- One tree per season. No competition between trees.

## Built with

JavaScript and HTML. Runs entirely in the browser, with no frameworks.

## Author

Sean Obiacoro — Mechanical Engineering (Systems Emphasis), University of Utah, May 2027
