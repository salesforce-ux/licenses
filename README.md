# Open Source License Agreements

Licensing guidelines for Salesforce UX open source projects.

## LICENSE files at the root of your projects

You may include these files in your projects.

- Source code should be released under BSD Clause-3 (see LICENSE.txt - make sure to change the YEAR)
- All icons and images are licensed under [Creative Commons Attribution-NoDerivatives 4.0](http://creativecommons.org/licenses/by-nd/4.0/) (see LICENSE-icons-images.txt)
- The font is licensed under our font license (see LICENSE-font.txt)

You should plan to engage with legal team if you intend to use a license other than BSD Clause-3.

## License Headers

The shorter version of license text should be added as a comment to all source code and configuration files that support comments.

```html
<!--
  Copyright (c) YEAR-present, salesforce.com, inc. All rights reserved
  Licensed under BSD 3-Clause - see LICENSE.txt or git.io/sfdc-license
-->
```

```js
/* 
  Copyright (c) YEAR-present, salesforce.com, inc. All rights reserved
  Licensed under BSD 3-Clause - see LICENSE.txt or git.io/sfdc-license
*/
```

```yaml
# Copyright (c) YEAR-present, salesforce.com, inc. All rights reserved
# Licensed under BSD 3-Clause - see LICENSE.txt or git.io/sfdc-license
```

## package.json

### Single License

Ideal for projects that only contain code, and don't include icons, images or fonts.

```json5
// package.json
{
  ...
  "license": "BSD-3-Clause",
  ...
}
```

### Multiple licenses

For projects like the Lightning Design System that include icons, images and fonts alongside the code.

#### package.json

```json5
{
  ...
  "license": "SEE LICENSE IN README.md",
  ...
}
```

#### README.md

This should appear at the bottom of the README.md file:

```md
## Licenses

* Source code is licensed under [BSD 3-Clause](https://git.io/sfdc-license)
* All icons and images are licensed under [Creative Commons Attribution-NoDerivatives 4.0](https://github.com/salesforce-ux/licenses/blob/master/LICENSE-icons-images.txt)
* The Salesforce Sans font is licensed under our [font license](https://github.com/salesforce-ux/licenses/blob/master/LICENSE-font.txt)
```

## Collaborator Contributions

Non-Salesforce contributors to our open source projects need to sign the Contributor License Agreement.

### Set up a webhook for the CLA bot

1. Go to the repository's **Settings › Webhooks**
2. Click **Add webhook**
3. Fill in the form  ![add-webhook](https://cloud.githubusercontent.com/assets/85783/22662023/69b3c3f2-ec5c-11e6-8739-366b9fae1380.png)
  - Payload URL: `https://cla.salesforce.com/webhook-pullrequest`
  - Content type: `application/json` 
  - Which events would you like to trigger this webhook?
    - Click **Let me select individual events**
    - **Uncheck "Push"**
    - **Check "Pull request"**
4. **Submit** the form

The CLA Bot will check new pull requests and make sure external contributors have signed the Salesforce Contributor License Agreement.
