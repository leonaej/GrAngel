# GrAngel World

An interactive web prototype for **GrAngel World**, a calm emotional-wellness experience for children. Kids pick a character, walk around a cozy village with GrAngel, the friendly heart-angel, and visit places full of gentle creative activities.

Plain HTML, CSS and JavaScript: no build step, no dependencies.

## Run it

Open `index.html` in a browser. To serve it locally instead:

```bash
npx serve .        # or: python -m http.server
```

## Project structure

```
index.html                        Entry screen ("Enter GrAngel World")
pages/
  home.html                       Village (home base)
  map.html                        World map of all places
  creativity-cottage.html         Creativity Cottage, outside
  creativity-cottage-inside.html  Creativity Cottage, inside (5 activities)
assets/
  images/                         Characters and GrAngel artwork
```

Each page is self-contained, with its CSS and JS inline.

## What's playable

- **Village**: choose a boy or girl character, walk with **W A S D** or the arrow keys, and follow the brick roads.
- **Map**: shows every place in the world. Places that aren't built yet are marked "coming soon".
- **Creativity Cottage**: go inside to find 5 stations: *Color & Create*, *Build-a-Scene*, *Story Builder*, *Color-the-GrAngel* and *Make-a-Melody*. There are no scores, only encouragement.

Pages share the chosen character and the sound and reduced-motion settings through `localStorage` (`grangelChar`, `grangelSound`, `grangelMotion`).

## Adding a new place

1. Create `pages/<place>.html`. Reference images as `../assets/images/...` and link back with `home.html`.
2. Add `page:'<place>.html'` to the place's entry in `LOCATIONS` in `pages/map.html`.
3. Add `page:'<place>.html'` to the matching road in `ROADS` in `pages/home.html`.

## License

See [LICENSE](LICENSE).
