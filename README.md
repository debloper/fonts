# Personal Font Server
To avoid getting door-slammed by Google Fonts.

[![](https://img.shields.io/badge/View_Repo-gray?logo=github)](https://github.com/debloper/fonts)

## Context
Google Fonts sometimes discontinues or deprecates fonts or its variants (e.g. Open Sans Condensed). This makes it problematic to "rely" on it on a long term basis, without risking occasional/prospective breaking of sites. And if it does happen and comes to the site maintainer's attention, it requires manual interventions to either replace the font with a similar substitute or resource it from some other online font distributor (like Adobe Fonts) if they have it available.

All in all, it's not a nice place to be; and I can't be arsed to micromanage the integrity of each font I've had used in various projects over the years, or in the future.

So, this repo when served over GitHub pages, without CORS restrictions (default behavior now) allows me to use my shortlist of fonts in my personal projects, without needing to worry about their continued availability.

## Usage
All fonts added here would have either canonical or converted WOFF2 format files. If they are converted, then it's done using [ttf2woff2](https://www.npmjs.com/package/ttf2woff2) (as of latest), but the original TTF/OTF formats are also preserved (just in case, if needed in future).

The TTF/OTF formatted fonts aren't generally meant to be used, even though can be. The WOFF2 files should be the ones to be used, as they're designed to be more optimal for the web.

Bulk conversion can be done with some like:
```bash
for f in *.ttf; do cat "$f" | ttf2woff2 > "${f%.ttf}.woff2"; done
```

## Disclaimer
This repository is free & open (see License section), but that's not to encourage being used as an alternative font distribution mechanism. That would be an antithesis to its own existence. Why would someone else "rely" on me (or this repo) to serve them fonts, expecting me to never delete/deprecate/discontinue/dislocate them any way I want and none of which is in their control? The reason this repo was created, is particularly to avoid that situation.

However, there's no intended or imposed restrictions from using it. I'll rather be happy if anyone does end up using it. But again, I promise nothing in terms of this as a distribution mechanism.

A better (rather, advisable) approach would be to fork the repo, remove/edit CNAME file, enable gh-pages, and use it as your own personal font server, if you want to.

## License
Unless otherwise mentioned, all the fonts in this repo are distributed under [SIL OFL](https://en.wikipedia.org/wiki/SIL_Open_Font_License). If any font uses a different permissive license, they'll be explicitly mentioned in their own subdirectories (it's super unlikely that a non-permissively licensed font will ever be added).

As for the repo itself, I don't want to create any License incompatibilities by assigning a parent license that can lead to unforeseen results because of distributing differently licensed fonts from it (and the repo itself can't have OFL, so there's a bit of an impasse). Personally I'd be OK with this being in the public domain (or [WTFPL](https://en.wikipedia.org/wiki/WTFPL)), but just in case it's important for any actual legal implication (just why!) assume CC0.

## Contributing
If you like the idea of having a personal font server, and decide to contribute, then:
- Please make sure you understand & agree with the license situation
- Create an issue for feature requests
- Create a pull request for submitting code changes
- Keep it simple and lean, avoid adding complexity
- Keep it function over form

I do intend to add an index page with ability to List, Search, Preview fonts etc. at some point, but that'll depend on how often do I feel the need for it, and how annoying I find the lack of it thereof. In the meantime, if you can't wait for that arbitrary time in future, then it's open for you to hop in & make it happen... Cheers!
