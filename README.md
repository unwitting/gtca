# GTCA
The Ghost Theme Configuration Approach: a unified method to allow Ghost blog admins to configure your themes.

Ghost themes which support __GTCA__ provide an easy-to-use method of configuring social profile links, commenting, analytics and more for blog admins. More than that, they are interopable: if an admin has configured their blog for one __GTCA__ theme, it should work with another one with __zero re-configuration__.

## Motivation
See the [original blog post](http://unwttng.com/introducing-gtca-make-your-ghost-themes-super-configurable/) for the rationale behind this and a more in-depth discussion.

## My theme supports GTCA!
You're a star. You should include something either in your theme or your theme's download page that tells people it's a __GTCA__ theme. This helps popularise the standard and allows interested blog admins to find out more.

Something like the following button works fine:

```html
<a
   href="https://github.com/unwitting/gtca"
   target="_blank"
   style="
     text-decoration: none;
     color: inherit;
     padding: 0.15em 0.25em;
     box-sizing: border-box;
     display: inline-block;
     border: 1px solid currentColor;
     border-radius: 0.25em;
   ">
  This theme supports <b>GTCA</b> configuration
</a>
```

![](https://dl.dropboxusercontent.com/s/xjd3f78y4fu66nc/Screenshot%202016-01-23%2011.08.42.png)

## The spec
Is simple. Your theme must meet a few requirements to be able to claim adherance to __GTCA__:

* `window.__themeCfg = {};` must exist somewhere in the code (or some functionally equivalent code that makes sure an empty `__themeCfg` object is assigned to the global scope).
* The above initialisation must come strictly before `{{ghost_head}}`. This allows configuration via header code injection.
* For any supported configuration property, document clearly to the user (either via their console logs, or in your theme help files) how to enable / set each one. This must assume little technical experience.
* You mustn't make use of properties which aren't in the [list](#gtca-configuration-properties) below. Using non-standard properties fools your users into thinking they're getting more interoperability between themes than they really are. If you need properties that aren't on the list yet, please raise a PR and it'll almost certainly be added nice and easily.

## GTCA configuration properties
Here's the current list of supportable __GTCA__ properties. To get more added, raise a PR against this README! The point isn't for me to control the list, it's for there to _be_ a list. Further social profiles, extra external integrations are all welcome. We just need to ensure that the configuration item/s allow for the full functionality to be achieved.

### Social profiles
* `__themeCfg.bitbucketUsername`
* `__themeCfg.deviantartUsername`
* `__themeCfg.facebookUsername`
* `__themeCfg.flickrUsername`
* `__themeCfg.githubUsername`
* `__themeCfg.instagramUsername`
* `__themeCfg.linkedinUsername`
* `__themeCfg.pinterestUsername`
* `__themeCfg.soundcloudUsername`
* `__themeCfg.twitchUsername`
* `__themeCfg.twitterUsername`
* `__themeCfg.vimeoUsername`
* `__themeCfg.youtubeUsername`

### Analytics
* `__themeCfg.googleAnalyticsId`

### Commenting
* `__themeCfg.disqusUsername`

### Publishing
* `__themeCfg.alternateSubscribeLink` - defines an alternative to the built-in RSS link (ex: [Feedburner](http://feedburner.google.com/) feed)
