# Typography theme for the Ghost CMS
## Version 1.0.0

### About Typography

Typography is my first theme for the Ghost CMS. I'll also make a version of it available for Wordpress (I'll post the link here when that's available).

I love Ghost! I love the simplicity of it, even though at this stage it's fairly limited in functionality, versus Wordpress anyway. Once we can build proper plugins for it, it will be amazing, and I'd love to see more businesses using it in the near future. With the advent of the Wordpress REST API, I'm sure it won't be long until someone figures out a way of using Ghost as a front-end to Wordpress's backend.

Typography is a minimalist theme, with a focus on typography, and an overarching aim of getting out of your way. It supports blog cover images, post feature images, social sharing on Facebook and Twitter, Disqus comment integration, and is fully mobile-ready.

### Installation and use

Installation is via the standard Ghost approach. Using git or FTP, or wget or curl, or whatever method you prefer, place the 'typographyghost' folder in your SITE_ROOT/content/themes folder. Reset Ghost and then select Typography in the Ghost admin panel (Settings -> General -> Theme), not forgetting to click Save. Typography is now your active theme.

### Selecting a font combination

Out of the box, Typography comes with twelve font combinations. On the most part the combinations include a serif font for headers, and a sans-serif font for body text. This isn't a hard and fast rule though, and some combos are serif-serif, and some are sans-serif-sans-serif.

The included font combinations are:

- Cheltenham & Cheltenham
- Cheltenham & Helvetica Neue
- Coco & Dubiel
- Coco & Helvetica Neue
- Couture & Dubiel
- Couture & Helvetica Neue
- Dubiel & Dubiel
- Dubiel & Helvetica Neue
- Helvetica Neue & Helvetica Neue
- Lustscript & Dubiel
- Lustscript & Dubiel
- Lustscript & Helvetica Neue
- Vanity & Dubiel

Sadly at this point Ghost doesn't allow developers to set theme options from inside the admin site, so in order to switch to a different font combination, you have to make a small change in the default.hbs file. To enable a specific fontsheet, with the default.hbs file (from line 20 onwards), simply uncomment your selection by removing the HTML commenting syntax from each end of the appropriate line. Be sure that all other fontsheet lines are commented out with HTML comments, except for the one that you want to use.

After changing the fontsheet, be sure to save default.hbs and re-upload it to the theme folder on your Ghost install. You will have to stop and start Ghost for the change to take affect.

More information on fontsheets, including how to use your own, can be found in the comments in default.hbs.

### Enabling Disqus comments

You'll need to register with Disqus, and have your Disqus shortcode to hand. Once you have this, open partials/disqus.hbs and add your shortcode where it says EXAMPLE. E.g. if your shortcode is myblogsite, then you would swap EXAMPLE.disqus.com with myblogsite.disqus.com. Save the file and re-upload it.

Now open post.hbs, and uncomment out line 15:

```
{{!-- {{> disqus}} --}}
```

should read:

```
{{> disqus}}
```

Save post.hbs and re-upload it to your Ghost install. Now restart Ghost, and Disqus commenting will be enabled.
