[//]: # (Copyright Jiaqi Liu)

[//]: # (Licensed under the Apache License, Version 2.0 &#40;the "License"&#41;;)
[//]: # (you may not use this file except in compliance with the License.)
[//]: # (You may obtain a copy of the License at)

[//]: # (    http://www.apache.org/licenses/LICENSE-2.0)

[//]: # (Unless required by applicable law or agreed to in writing, software)
[//]: # (distributed under the License is distributed on an "AS IS" BASIS,)
[//]: # (WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.)
[//]: # (See the License for the specific language governing permissions and)
[//]: # (limitations under the License.)

Aergia Documentation
--------------------

This website is built using [Docusaurus 2](https://docusaurus.io/), a modern static website generator.

### Installation

```bash
yarn
```

### Local Development

```bash
yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without
having to restart the server.

### Build

```bash
yarn build
```

This command generates static content into the `build` directory and can be served using any static contents hosting
service.

### Deployment

Using SSH:

```bash
USE_SSH=true yarn deploy
```

Aergia is using GitHub pages for hosting, this command builds the website and push to the `gh-pages` branch.

### Troubleshooting

#### Docusaurus Blogs Relative Linking is Treated False-Negative by CI Markdown Link check

[CI check for Markdown link](../.github/workflows/ci-cd.yml) (`markdown-link-check`) is turned on and it's not smart
enough to detect relative linking by Docusaurus. The workaround is to disable the link check at the relevant line. For
example:

```markdown
<!-- markdown-link-check-disable -->
known. Additionally, this process makes it easy to implement a [blue-green deployment](continuous-delivery) or
<!-- markdown-link-check-enable -->
```
