# Third Party Notices

Lumenfolio bundles selected third-party components in desktop release artifacts.
This notice records the bundled PDF translation sidecar used by the release
workflow.

## PDFMathTranslate / pdf2zh Sidecar

- Component: PDFMathTranslate / PDFMathTranslate-next / pdf2zh sidecar runtime
- Upstream source: https://github.com/PDFMathTranslate/PDFMathTranslate-next
- Local source path: `external/PDFMathTranslate/pdf2zh/kernel/PDFMathTranslate-next.git`
- License: GNU Affero General Public License v3.0
- License text: `external/PDFMathTranslate/pdf2zh/kernel/PDFMathTranslate-next.git/LICENSE`

The GitHub Actions release workflow checks out the upstream source as a git
submodule and builds a private sidecar runtime for each desktop platform. The
workflow does not patch or modify PDFMathTranslate/pdf2zh source code.

Release artifacts that include this sidecar are accompanied by this notice, the
AGPL license text, and a `PDFMathTranslate-next-source.tar.gz` archive generated
from the submodule commit used to build the sidecar. Recipients can rebuild the
bundled runtime with:

```bash
npm run build:pdf2zh-runtime:macos
npm run setup:pdf2zh
npm run build:pdf2zh-runtime:windows
```

The main Lumenfolio application is also licensed under the GNU Affero General
Public License v3.0, matching the bundled PDFMathTranslate/pdf2zh sidecar.
