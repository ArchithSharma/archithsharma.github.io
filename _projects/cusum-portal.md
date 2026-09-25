---
title: "CUSUM Portal: Spatio-Temporal Earthquake Anomaly Detection"
collection: projects
status: current
permalink: /projects/cusum-portal/
order: 0
excerpt: "An in-progress anomaly-detection portal that flags abnormal seismic swarms in live USGS earthquake data using spatio-temporal CUSUM change detection. Research with Dr. Woody Zhu, supported by SURF."
---

Ongoing research with **Dr. Woody Zhu**, supported by **SURF**.

## What it does

The portal applies sequential change detection to live earthquake catalogs to flag unusual bursts of seismic activity:

1. Fetches live [USGS GeoJSON earthquake feeds](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php).
2. Groups events into spatial grid cells and aggregates them over uniform time steps.
3. Converts magnitudes to an energy proxy using the Gutenberg–Richter relation, $$E \propto 10^{1.5M}$$
4. Runs a one-sided CUSUM on each cell's energy series,

   $$S_t = \max\left(0,\; S_{t-1} + (X_t - \mu_0 - k)\right),$$

   and raises an alarm when $$S_t > h$$, where $$\mu_0$$ is the cell's baseline mean energy, $$k$$ is a slack allowance and $$h$$ is the decision threshold (both scaled by the cell's standard deviation).
5. Reports flagged cells and maps the anomaly zones over the epicenters.

## Links

[Open the portal](https://archithsharma.github.io/cusum_portal_draft/){: .btn} [View the code on GitHub](https://github.com/ArchithSharma/cusum_portal_draft){: .btn}
