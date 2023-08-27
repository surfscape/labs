---
title: AdZone
track_code: SPTC070523SSA-AZ
date: 2023-05-07T00:00
summary: Promotion platform using ad banners
status: Hiatus
---

A promotion platform for users to promote their personal site trough ad banners.

## Implementation Idea

AdZone would consist on a `iFrame` that users can add to their site where every `x` seconds the ad banner would change. If the user clicks on the banner it would go to that banner site on a new tab.

The banner would be made by the user which could be uploaded to a public file host. The user then would send the banner link and the site information (url and title) trough GitHub issues or PRs. A email option would also be available but that is still pending.

The banner can be either a `webp` for simple banners but also animated banners using either `gif` or `webp`.

The code would simply go trough a `.json` database with all the joined websites like this:

<div class="pre-container">

```json
{
  "adBanner": [
    {
      "title": "SurfScape",
      "url": "https://surfscape.github.io",
      "banner": "https://imagehost.com/surfscape_banner.gif"
    }
  ]
}
```

and after some amount of time it would go to the next item in the array using a `for` loop.

</div>

## Notes

AdZone is part of the [SurfScape Advertising](https://surfscape.github.io/advertising/) project which can be seen by the track code having `SSA-AZ` (SurfScape Advertising - AdZone).
SSA already as a page for [AdZone](https://surfscape.github.io/advertising/adzone/) with additional information. However this site will be deprecated with a new version using the SurfKit UI framework.
