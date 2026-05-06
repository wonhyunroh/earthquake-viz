---
layout: default
title: "The Earth Doesn't Sit Still: 30 Days of Global Earthquakes"
---

# The Earth Doesn't Sit Still

## 30 Days of Global Earthquakes, and What They Tell Us About the Planet We Live On

**By Inseo Song (inseos2) and Won Roh (wonhyun2)**

*Final Project Part 3.1, Spring 2026*

---

## A planet that never stops shaking

In just 30 days, between March 30 and April 28, 2026, the U.S. Geological Survey recorded **571 earthquakes** of magnitude 4.5 or greater somewhere on Earth. That works out to about **19 sizable quakes every single day**, most of which you probably never heard about. Some happened far from any major city. Others happened on the ocean floor. A few were strong enough to make the news, but most were not.

We were curious where all of these earthquakes are actually happening. Are they evenly spread out across the planet? Or is there a pattern? It turns out the answer is pretty striking once you put every quake on a map.

In this article, we use the past 30 days of USGS data to walk through what we found. The main map below is interactive: you can hover over any dot to see exactly when and where that earthquake happened, zoom into a region, or pan around the globe.

---

## Map: every M4.5+ earthquake in the past 30 days

Each dot is one earthquake. The position is the epicenter (where the earthquake started). Color and size both encode magnitude, so the strongest quakes show up as the biggest, darkest red dots.

<iframe src="earthquake_map.html" width="100%" height="640" frameborder="0" style="border:1px solid #e1e4e8; border-radius:6px;"></iframe>

*Source: USGS Earthquake Catalog. Visualization created by the authors using Plotly.*

### A pattern jumps off the map

Step back from the map for a second and just look at the dots. They aren't scattered evenly. They trace a clear arc around the Pacific Ocean, run down the western coast of South America, and cut across Indonesia, Japan, and the Philippines. Geologists call this band the **"Ring of Fire"**, and it's home to roughly 90% of the world's earthquakes.

The reason becomes obvious once you compare our map to a map of the planet's tectonic plates.

---

## Context: Earth's tectonic plates

Earth's outer shell is broken up into a dozen or so giant slabs of rock, called tectonic plates. The plates are slowly moving, and where they push, pull, or grind against each other, the friction builds up over years until it's released as an earthquake. That's why earthquakes don't happen randomly: they happen along the lines where these plates meet.

![Tectonic plates of the world](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8a/Plates_tect2_en.svg/1280px-Plates_tect2_en.svg.png)

*Map of Earth's major tectonic plates and their boundaries. Source: USGS, public domain, via [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Plates_tect2_en.svg).*

If you flip back and forth between this plate map and our earthquake map above, the match is almost perfect. Nearly every cluster of red dots sits directly on a plate boundary. Inland regions like central Russia or central Africa, far from any plate edge, see almost no quakes at all. The dots are basically tracing the seams of the planet.

---

## Which countries shook the most?

To make the geographic concentration even more concrete, here's the top 10 countries and regions in our 30-day window, ranked by the number of M4.5+ earthquakes recorded.

<iframe src="top10_regions.html" width="100%" height="540" frameborder="0" style="border:1px solid #e1e4e8; border-radius:6px;"></iframe>

*Chart created by the authors from the USGS Earthquake Catalog. Region names were extracted from the USGS `place` field by taking the text after the final comma.*

**Indonesia alone accounts for roughly 28% of all M4.5+ earthquakes in this window**, almost three times more than the next country (Japan, with 50). That's not because Indonesians are unlucky. It's because Indonesia sits at the meeting point of three major tectonic plates: the Indo-Australian, the Eurasian, and the Pacific plates. Japan and the Philippines are similarly squeezed between plates, which is why they round out the top of the list.

---

## What this means for you

The good news is that magnitude alone doesn't tell the whole story. Many of the earthquakes on the map above happened **deep below the surface**, sometimes hundreds of kilometers down, where they're rarely felt by people on land. Others happened in the open ocean, far from anyone. The earthquakes that actually matter day-to-day are the **shallow** ones (less than 70 km deep) that strike near populated areas. Try zooming into Indonesia or Japan on the map and hovering on the dots to see how varied the depths really are.

Earthquake science isn't just academic either. Knowing exactly where earthquakes cluster is what tells governments where to require stricter building codes, where to put early-warning sensors, and how to plan evacuation routes. Most of Japan's famously earthquake-resistant architecture exists because Japan, statistically, has had no other choice.

So the next time you see an earthquake headline from somewhere along the Ring of Fire, you'll know it isn't a freak event. It's the planet doing exactly what it's been doing for billions of years: shifting, grinding, and very occasionally reminding the people on top that the ground beneath them isn't quite as solid as it seems.

---

## Data and code

- **Primary dataset:** USGS Earthquake Catalog (M4.5+, past 30 days). The exact CSV used here is included in this repo: [USGS_EarthQuake.csv](USGS_EarthQuake.csv).
- **Analysis notebook:** [View on GitHub](Workbook.ipynb). All charts on this page are produced by the notebook.
- **Tectonic plate boundary map (image):** USGS, public domain, via [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Plates_tect2_en.svg).
- **Tectonic plate boundary dataset (referenced for further reading):** Hugo Ahlenius, *World tectonic plates and boundaries*, [github.com/fraxen/tectonicplates](https://github.com/fraxen/tectonicplates).
- **"Ring of Fire" background reading:** USGS, [Ring of Fire](https://www.usgs.gov/faqs/what-ring-fire).

---

*Built with Jekyll and Plotly. Inseo Song and Won Roh, 2026.*
