# Turning Data Center Waste Heat into Drinking Water

Everyone talks about how much electricity AI consumes. Almost nobody talks about the water. Once I started looking closely, I saw the issue everywhere: data centers being denied water permits, drought-hit communities pushing back against new AI campuses, and major companies quietly competing for water rights to power their server farms. It wasn't some abstract future concern. It was already happening, right now, in real places and real communities.

That realization pushed me to build something small but meaningful on my workbench — a working prototype to show that the waste heat from compute infrastructure could be used to generate clean water.

## The Problem

AI infrastructure doesn't just consume electricity; it also demands enormous amounts of water for cooling. By 2025, data centers supporting AI workloads were already using nearly one trillion liters of water each year, with evaporative cooling systems making up the biggest share of that consumption.

This problem is not evenly distributed. Northern Virginia, for example, is the largest data center hub in the world, and during summer months data centers account for more than 11% of industrial water use in Loudoun County. In places like that, water is not just an operational input — it's a shared local resource under stress.

Then there is the hidden cost: the electricity that powers AI infrastructure also requires water at power plants, especially thermal plants. So the true water footprint of AI is not only the water used on-site, but also the water used to generate the electricity feeding those servers in the first place.

That was the question that stayed with me: if these systems already generate so much waste heat, why not use it instead of letting it vanish into the air?

## My Approach

Instead of treating waste heat as a problem, I decided to use it as a resource. I explored methods of heat recovery and kept coming back to distillation as the cleanest and most testable concept: use heat to evaporate water, leave contaminants behind, and then condense the vapor back into purified liquid.

I designed a small prototype using an ESP32 as a stand-in for a real compute load. It generates heat continuously, much like a server rack, and the system around it simulates a real-world waste-heat recovery setup.

The core idea is simple:

- Dirty or saline feed water is placed in a sealed chamber.
- A heater at the bottom raises the water temperature until it evaporates.
- Only pure water vapor rises, leaving salts and contaminants behind.
- The vapor condenses on a cooler angled lid and slides down into a clean collection cup.

I also used the ESP32 to control the system with a relay and a waterproof temperature sensor, adding safety logic to prevent overheating. The design even recycles some of the released condensation heat to pre-warm the next batch of feed water, making the cycle more efficient.

## Prototype and Build

<p align="center">
  <img src="Gallery/water_still_project_poster.png" width="760" alt="Waste heat distillation project poster" />
</p>

<p align="center">
  <img src="Gallery/model.png" width="420" alt="Prototype front view" />
  <img src="Gallery/model2.png" width="420" alt="Prototype side view" />
</p>

## What I Learned

This project taught me more than I expected. It forced me to think about heat transfer, safety cutoffs, thermal gradients, insulation, and build quality in a way that wasn't theoretical. It isn't just about turning a heater on — it's about making the process stable, efficient, and safe.

I also learned that the real goal is not to eliminate waste heat completely, but to make sure whatever heat is produced gets used at least once before it disappears. That mindset is useful far beyond this project and applies to industrial systems, energy planning, and sustainable engineering in general.

Every failed seal and every weak condensation cycle taught me something practical. Physical systems do not behave like ideal textbook examples. Building them means iterating, debugging, and learning through the process itself.

## Why This Matters

My prototype produces only a small amount of water, and that was never the point. The purpose was to prove, at a small scale, that the waste byproducts of modern infrastructure do not have to remain waste.

If a student with a few hundred rupees worth of parts and a weekend can build a functioning demonstration, then it raises a much bigger question: what could a properly resourced engineering team do at real scale with the same concept?

As AI infrastructure keeps expanding, ideas like heat recovery, circular resource loops, and smarter cooling systems are going to matter more, not less. This project was my hands-on attempt to explore that direction.

<p align="center">
  <img src="Gallery/mini_data_center_water_still.png" width="760" alt="Mini data center water still concept" />
</p>

<p align="center">
  <strong>— Aman Mehta</strong>
</p>

