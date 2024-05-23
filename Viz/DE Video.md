# Destination Earth outreach.
Handling the discussions in our [gitlab](https://earth.bsc.es/gitlab/otintopr/visualization)

## Tasks

- [ ] Data handling:
	- [x] Make a tool to handle all texture generation:
	- [ ] Explore getting the helpix grid and plotting it directly without previous interplation using Healpy.

 - [x] Sea-ice data has been completed (ice-thick + tos)
- [ ] Hurricanes:
	- [ ] 2025: October 
	- [ ] 2027: 25 August -> 5 sept

- [ ] ENSO:
	- [ ] How do I slow down the ocean?
	- [x] Baking the particles from command line: can inspect the bake node with the debug options enabled.
	- [ ] Try particles with ocean currents:
		- [ ] Reuse windy.
		- [ ] Change winds to currents.
		- [ ] Remove particles on Earth
		- [ ] Use object controller to keep only particles in a certain region.

	I have the data from early 2021 to mid 2023, a full transition from ENSO+ to ENSO- (a71p)
- [ ] Intro:
	- [x] Use realistic Earth and do a cinematic spin to the Earth moving the camera instead of rotating the Earth.

	- [x] Make a "photorealistic" Earth using clouds, sea-ice and snow. 
	- [x] Make it renderable in MN5.
	- [x] Temporal Supersampling in MN5?
	      Able to run RIFE relying on micromamba to setup the environment.
- [x] Prepare temperature and msl data for the "identified" heatwave: July 2021
- [x] Made an addon to quickly import colormaps.