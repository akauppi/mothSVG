# Devs

This file has notes about the "internals" and the psyche of the project. Not needed to use it. Could be nice for developers and contributors.


## Design criteria

- Use just one JavaScript environment

	SVG has its own JavaScript environment, but this differs from the browser's normal environment in many ways, and has never really caught up the wind. Don't require people to learn it. Instead, have the logic run in the normal (HTML) JavaScript environment.

- Animation matters

	Make animating single wiggle and other animations as easy as adding a `wiggle` class name (no code).
	
- Touch first

	We aim at tablets and phones. In addition, a mouse based system should work.

- Allow external SVG editors

	For the creation of assets, it's important any desktop or online SVG editor can be used.

- Derive from Svelte 3's mindset
  - animation is cool and 1st class citizen
  - size and performance matters - a lot (enables wider use opportunities)



## Notes

### No `package-lock.json`

It's unclear if it's really that needed/useful. It does cause problems e.g. if `package.json` is directly edited (which... of course we do!):

>However, this only happens if you use NPMs’ CLI to make changes. If you manually change package.json, don’t expect package-lock.json to update. Always use the CLI commands, like install, uninstall, etc. <sub>[source](https://blog.logrocket.com/why-you-should-use-package-lock-json/)</sub>

