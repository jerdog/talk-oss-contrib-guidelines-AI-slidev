# Jeremy's base Slidev talk deck

## Dependencies

- Slidev - https://sli.dev/
- 


## Using & Development

1. [Fork] (https://github.com/jerdog/jerdog-base-talk-slidev/fork) the repo to your organization

2. Clone the repo

```bash
git clone <your fork>
cd <your local fork directory>
```

3. Install dependencies and run the dev server

```bash
npm install
npm run dev
```

4. View the base: <http://localhost:3030>

5. Edit the [slides.md](./slides.md) file and then save to see the changes.

Learn more about Slidev at the [documentation](https://sli.dev/).

### Config items

#### Main presentation

For the presentation config, edit the specific YAML entries in the [slides.md](./slides.md) frontmatter:

- `theme:` by default using the `slidev-theme-the-unnamed` theme
- `title:` 
- `author:`
- `info:` this block is markdown and is where to put basic info (title, abstract, etc.)
- `conference:` put the conference name, which will be used in the left footer of the presentation
- `keywords:` put the keywords for the presentation
- `favicon:` put the favicon for the presentation, can be a local file or a URL

**Other config items**

- `fonts:` a list of values for the font types (sans, serif, mono) to use in the presentation
- `class:` the default class for the presentation
- `defaults:` default frontmatter for the presentation (layout, transition, etc.)

#### Presentation slides

The slides are written in markdown and HTML, and each slide begins with a `---` line. You can use frontmatter to add additional information to the slide by adding it after the `---` line, and then closing the frontmatter with another `---` line.

You can add specific config for each slide like class, layout, transition, etc.

### Addons

There are a few addons which make sense for these slides, and you include them in the presentation by adding them to the `addons` list in the [slides.md](./slides.md) frontmatter:

```yaml
addons:
    - slidev-addons-rabbit
```

- [slidev-addon-qrcode](https://www.npmjs.com/package/slidev-addon-qrcode) - add a QR code to the slide
***Note:*** use the `<div>` with the class to center the rendered qr code. Remove the `image="/logo.svg"` parameter if you don't want a logo in the center.

```html
<div class="flex flex-col items-center">
    <QRCode
        :width="100"
        :height="100"
        type="svg"
        data="https://sli.dev"
        :margin="10"
        :imageOptions="{ margin: 10 }"
        :dotsOptions="{ type: 'extra-rounded', color: 'purple' }"
        image="/logo.svg"
    />
</div>
```

- [slidev-addon-rabbit](https://www.npmjs.com/package/slidev-addon-rabbit) - add a rabbit at the bottom of the slide which progresses from left to right according to the time you have set with the `?time=xx` with `xx` being the number of minutes for the presentation. If you want the slide number to be shown with the rabbit, add the following to the slide config frontmatter:

```yaml
rabbit:
  slideNum: true
```

## LICENSE

MIT License

Copyright (c) 2024-25 Jeremy Meiss.