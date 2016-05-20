# Performance Optimized Material Design Lite theme for Hugo

This is a theme for [hugo](https://gohugo.io), a static site generator. It is based on the [blog template](https://www.getmdl.io/templates/) of Google's [Material Design Lite](https://www.getmdl.io).

[![wercker status](https://app.wercker.com/status/7ad5c12955820fb82aa3e34021d07ac8/m "wercker status")](https://app.wercker.com/project/bykey/7ad5c12955820fb82aa3e34021d07ac8)

### TODO

- [x] Use a service-worker.js for stellar performance
- [x] Add top-menu (top right on desktop)
- [x] inline SVG icons to replace external PNG
- [x] Remove external background image
- [ ] Remove external font and CSS for share buttons (latest version of share buttons has that)
- [ ] Set primary and accent color (with SASS)
- [x] Use local Font (Roboto)
- [x] Use local Font (Material Design Icons)
- [x] Add Google Tag Manager (GTM) support
- [x] Gulp integration (gets you minified and concatenated assets)
- [ ] Auto reload & re-run Gulp
- [ ] Add word count
- [ ] Test code highlighting

### Usage

    cd hugo/themes
    git clone https://github.com/Joostvanderlaan/material-design-lite-performance.git

### Content organization & features

This theme does currently **not support** lists, categories, tags...

This theme is optimized to use 2 content types: `post`s and `page`s. Pages are automatically displayed in the dropdown list beneath the author and posts are displayed on the homepage.

You can add a `description` and an `image` to a post or page using the front matter.

### Some features

* posts can have featured images
* header contains tags for [Open Graph](http://ogp.me/) and [Twitter Cards](https://dev.twitter.com/cards/overview)
* links to profiles on Facebook, Twitter, Google Plus
* customizable share button
* pagination
* customizable background image/color
* customizable design (colors)
* responsive design
* code highlighting

### Configuration variables

These are the supported site parameters:

```TOML
	
	[params]
		TwitterUser = "YourTwitterUsername"
		FacebookUser = "YourFacebookUsername"
		GooglePlusUser = "YourGooglePlusUsername"
		copyright = "&copy; 2016 A short copyright statement"
		author = "Joost van der Laan"
		background = "/images/beach-jl.jpg" # a relative or absolute URL to a background image
		bgcolor = "a background color; will be ignored if you use background"
		primary = "indigo"
		accent = "pink"
		# Tag of GA & GTM will hide if unset.
		GoogleAnalytics = "UA-XXXXXXXX-X"
		GoogleTagManager = "GTM-XXXXXX"
```

*Primary* and *accent* define the colors of the design. Check [the MDL customizer](https://www.getmdl.io/customize/index.html) to see the supported colors.

### Share button configuration

Create a file called *share.html* in *layouts/partials/* to override the configuration for the share button.

This is the default configuration. This button uses a plugin called *carrot* to share to different networks. I recommend keeping the `ui` part as is and only modifying the `networks` part. Check [this link](https://github.com/carrot/share-button/wiki/Configuration-Options) for detailed instructions.

	<script>
		// See https://github.com/carrot/share-button/wiki/Configuration-Options
		$(function() {
			var config =
				{
					ui: {
						flyout: "middle left",
						button_text: "<i class='material-icons'>share</i>"
					}
			};
			var share = new Share(".share", config);
		});
	</script>

### Header tags

If you want to add extra tags to the `<head>` of your page, you can create a file called *header-extra.html* in *layouts/partials/* and add your extra content to that file.

### Contributing

You want to contribute? That's awesome! ❤ Please create an issue or a pull request to contribute.

### Demo

https://somedemolinkhere.joostvanderlaan.nl

### Code

https://github.com/Joostvanderlaan/material-design-lite-performance

### License

Like the original template, this theme's license is Apache 2.0.
