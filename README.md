PLANETARY LAB

Earth analogue intelligence, planetary terrain analysis and rover mission simulation. Built for the NASA Space Apps Challenge: Identify Earth Locations that Analog the Permanent Moon Base Locations and Mars.

Team: Shobhit Utkarsh Kujur, Vaibhav Kanth, Ayush Minz

What it is

PLANETARY LAB is a decision-support tool that answers two linked questions:

Which places on Earth look like the Moon or Mars, and how much do they really match?
How would a real rover design behave on those terrains, and would a modification actually help?

It has three parts:

Part	What it does	Where
Rover simulator	Loads NASA’s Perseverance rover as a baseline, lets you modify wheels, mass, battery, insulation and shielding, and compares both rovers on the same terrain. It calculates slope climbing, traction, wheel slip, soil sinkage, energy, temperature and radiation dose, and shows the result in 3D with craters, rocks and boulder fields.	index.html
Terrain and analogue engine	Turns elevation files into slope, roughness and terrain-class statistics and scores how closely an Earth site matches a Moon or Mars target. Missing data is never counted as zero: it lowers a reported coverage figure.	python/
JARVIS assistant	A text assistant in assist mode. It answers by running the same calculations as the page, and it cannot drive the rover.	index.html

You can also upload your own elevation file (GeoTIFF) and simulate any location.

Why it matters
Space agencies test hardware and train crews on Earth. NASA runs field research at analogue sites such as Devon Island in Arctic Canada, home of the Haughton impact crater and the Haughton-Mars Project. Choosing where to test is a major decision.
No Earth site matches fully. Gravity, air pressure and radiation cannot be reproduced on Earth, so a site can be a good terrain match and a poor thermal or radiation match. This project reports both what matches and what does not, with the data coverage behind every score.
Rover performance depends on the world it drives on. The same machine slips and sinks differently under lunar, Martian and Earth gravity. Simulating that before field trials shows trade-offs early, for example that bigger wheels can cross taller rocks but add mass.
It is transparent. Every value carries a status: published, derived, modelled or scenario. Nothing is presented as measured when it is an assumption, and the whole workflow can be reproduced from the files in this repository.
