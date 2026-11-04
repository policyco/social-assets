# social-assets

Public image hosting for [PolicyCo](https://policyco.io) social posts.

Buffer needs a publicly reachable image URL to create Instagram drafts, so every image used in a PolicyCo post on Instagram, LinkedIn or X lives here and is referenced by its raw GitHub URL.

> **This repo is public.** Put only finished, approved marketing images here. No customer data, screenshots with real tenant content, internal docs or anything you wouldn't post on LinkedIn yourself.

## Using an image

Reference files by their raw URL on `main`:

```
https://raw.githubusercontent.com/policyco/social-assets/main/<topic>/<file>
```

For example:

```
https://raw.githubusercontent.com/policyco/social-assets/main/municipal/01-version-control-instagram.png
```

Don't rename or move a file once a post points at it. Drafts and scheduled posts in Buffer will break if you do. Add a new file instead.

## Layout

One folder per topic or campaign. The folder name is the same slug used for `utm_content` on that campaign's links (e.g. `municipal` → `utm_content=municipal`).

```
<topic>/
  <NN>-<short-slug>-<platform>.<ext>
```

- `NN`: the post's position in the series (`01`, `02`, …). The same number is used on every platform so one post keeps one image across channels.
- `short-slug`: a few words describing the post, lowercase and hyphenated.
- `platform`: `instagram`, `linkedin` or `x` (`youtube` for the rare video thumbnail).

```
municipal/
  01-version-control-instagram.png
  01-version-control-linkedin.png
  01-version-control-x.png
  02-council-approval-instagram.png
  ...
```

## Sizes

Crop each image for its platform rather than relying on the platform to do it.

| Platform  | Size (px)   | Ratio  | Notes                                   |
|-----------|-------------|--------|-----------------------------------------|
| Instagram | 1080 × 1350 | 4:5    | Portrait gets the most feed space. 1080 × 1080 is fine too. |
| LinkedIn  | 1200 × 627  | 1.91:1 | 1200 × 1200 square also works well in the feed. |
| X         | 1600 × 900  | 16:9   | Keep text away from the edges, since previews crop. |

- Use PNG for graphics with text and JPG for photos.
- Keep files under 5 MB. Instagram rejects anything over 8 MB.

## Look and feel

- Campaign art follows the brand's Art Deco / WPA industrial poster style: angular geometry, earth tones (burnt orange, pea green, gray-blue, deep ochre), high-contrast shadows.
- Product UI shots match the product itself (same fonts, colors and badges) rather than the poster style.
- Brand purple is `hsl(266 25% 54%)` / `#866CA7`. The logo goes on top of it in all-white.
