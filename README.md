# GTCA
The Ghost Theme Configuration Approach: a unified method to allow Ghost blog admins to configure your themes.

Ghost themes which support __GTCA__ provide an easy-to-use method of configuring social profile links, commenting, analytics and more for blog admins. More than that, they are interopable: if an admin has configured their blog for one __GTCA__ theme, it should work with another one with __zero re-configuration__.

## Motivation
See the [original blog post](http://unwttng.com/introducing-gtca-make-your-ghost-themes-super-configurable/) for the rationale behind this and a more in-depth discussion.

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
