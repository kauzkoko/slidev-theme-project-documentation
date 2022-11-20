---
theme: ./
layout: intro
image: 'https://source.unsplash.com/collection/94734566/1920x1080'
projectTitle: 'Documentation Template'
subtitle: 'Use this slidev template for your project documentations.'
header: 'Created in 2022'
---
---
layout: text-1-image
image:  'https://source.unsplash.com/collection/94734566/1920x1080'
caption: 'image from unsplash api'
linkSrc:  'https://source.unsplash.com/collection/94734566/1920x1080'
---

## Layout: text-1-image

Simple layout with title, text and an landscape format image with optional caption.
The image links to an online source.

Use following props in FRONTMATTER/YAML zone:
- image: '[YOUR URL]'
- linkSrc: '[YOUR URL]'

---
layout: text-2-images
image1: 'https://source.unsplash.com/collection/94734566/1080x1920'
caption1: 'Top picture: unsplash api'
linkSrc1:  'https://source.unsplash.com/collection/94734566/1920x1080'
image2: 'https://source.unsplash.com/collection/94734566/1080x1920'
caption2: 'Bottom picture: unsplash api'
linkSrc2:  ''
---

## Layout: text-2-images

Simple layout with title, text and 2 non linking landscape format images with optional caption.

Use following props in FRONTMATTER/YAML zone:
- imageTop: '[YOUR URL]'
- caption1: '[YOUR CAPTION]'
- imageBottom: '[YOUR URL]'
- caption2: '[YOUR CAPTION]'

---
layout: 2-images-portrait
imageTop: 'https://source.unsplash.com/collection/94734566/1080x1920'
caption1: 'Top picture: unsplash api'
imageBottom: 'https://source.unsplash.com/collection/94734566/1080x1920'
caption2: 'Bottom picture: unsplash api'
---

## Layout: 2-images-portrait

Simple layout with 2 images in portrait format and optional caption.

Use following props in FRONTMATTER/YAML zone:
- imageTop: '[YOUR URL]'
- caption1: '[YOUR CAPTION]'
- imageBottom: '[YOUR URL]'
- caption2: '[YOUR CAPTION]'

---
layout : 3-images
imageLeft: 'https://source.unsplash.com/collection/94734566/1080x1920'
imageTopRight: 'https://source.unsplash.com/collection/94734566/1080x1920'
imageBottomRight: 'https://source.unsplash.com/collection/94734566/1080x1920'
---

## Layout: 3-images

Simple layout with 3 images. 1 portrait format image on the left and 2 landscape format images on the right.

Use following props in FRONTMATTER/YAML zone:
- imageLeft: '[YOUR URL]'
- imageTopRight: '[YOUR URL]'
- imageBottomRight: '[YOUR URL]'

---
layout: 4-images
image1: 'https://source.unsplash.com/collection/94734566/1080x1920'
caption1: 'Left: unsplash api'
linkSrc1:  'https://source.unsplash.com/collection/94734566/1920x1080'
image2: 'https://source.unsplash.com/collection/94734566/1080x1920'
caption2: 'Right: unsplash api'
linkSrc2:  'https://source.unsplash.com/collection/94734566/1080x1920'
image3: 'https://source.unsplash.com/collection/94734566/1080x1920'
caption3: 'Left: unsplash api'
linkSrc3:  'https://source.unsplash.com/collection/94734566/1920x1080'
image4: 'https://source.unsplash.com/collection/94734566/1080x1920'
caption4: 'Right: unsplash api'
linkSrc4: 'https://source.unsplash.com/collection/94734566/1080x1920'
---

## Layout: 4-images

Simple layout with 4 images in landscape format and optional caption.

Use following props in FRONTMATTER/YAML zone:
- image1: '[YOUR URL]'
- linkSrc1: '[YOUR URL]'
- caption1: '[YOUR CAPTION]'
- image2: '[YOUR URL]'
- linkSrc2: '[YOUR URL]'
- caption2: '[YOUR CAPTION]'
- image3: '[YOUR URL]'
- linkSrc3: '[YOUR URL]'
- caption3: '[YOUR CAPTION]'
- image4: '[YOUR URL]'
- linkSrc4: '[YOUR URL]'
- caption4: '[YOUR CAPTION]'
