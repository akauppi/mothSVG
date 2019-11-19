# Devs

This file has notes about the "internals" and the psyche of the project. Not needed to use it. Could be nice for developers and contributors.


## Design criteria

- Use just one JavaScript environment

	SVG has its own JavaScript environment, but this differs from the browser's normal environment in many ways, and has never really caught up the wind. Don't require people to learn it. Instead, have the logic run in the normal (HTML) JavaScript environment.

- Animation matters

	Make animating single wiggle and other animations as easy as adding a `wiggle` class name (no code).
	
- Touch first

	We aim at tablets and phones. In addition, a mouse based system should work.

- Derive from Svelte 3's mindset
  - animation is cool and 1st class citizen
  - size and performance matters - a lot (enables wider use opportunities)



