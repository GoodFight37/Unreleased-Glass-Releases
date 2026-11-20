# Third-Party Notices

**Unreleased Glass** uses third-party software. The project's own
source code is licensed under the MIT License (see [LICENSE](LICENSE)). The
components listed below retain their own licenses, which are reproduced or
linked here to satisfy their attribution and distribution terms.

If you distribute a build of this application, keep this file (and the
FFmpeg notice in particular) with the distribution.

---

## FFmpeg — GNU General Public License v3.0 (IMPORTANT)

Desktop builds obtain a prebuilt **FFmpeg** binary on first use for local
audio format conversion. Development builds can reuse the copy installed by
[`ffmpeg-static`](https://github.com/eugeneware/ffmpeg-static). The current
installer configuration does not bundle these optional tool binaries. This
FFmpeg binary is licensed under the
**GNU General Public License, version 3.0 or later (GPL-3.0-or-later)**.

The application invokes FFmpeg as a **separate command-line subprocess**.
The FFmpeg binary retains its own license. Any distribution that includes
that binary must comply with the applicable GPL terms, including:

- **License text.** FFmpeg is Copyright (c) the FFmpeg developers and
  contributors. The full text of the GNU General Public License v3.0 is
  available at <https://www.gnu.org/licenses/gpl-3.0.txt> and is included with
  the FFmpeg distribution.
- **Corresponding source.** Redistributors must provide the corresponding source
  for the exact binary they distribute, using a method permitted by its license.
  The current download comes from the
  [ffmpeg-static b6.1.1 release](https://github.com/eugeneware/ffmpeg-static/releases/tag/b6.1.1).
  General upstream references are <https://ffmpeg.org/download.html> and
  <https://git.ffmpeg.org/ffmpeg.git>; these links alone are not an offer of
  corresponding source for an arbitrary binary.
- **No warranty.** FFmpeg is distributed WITHOUT ANY WARRANTY; see the GPL for
  details.

FFmpeg is a trademark of Fabrice Bellard, originator of the FFmpeg project.
More information: <https://ffmpeg.org>.

---

## Optional yt-dlp downloader

The URL-import tool downloads **yt-dlp** when requested and reuses an existing
installed copy. Its binary and SHA-256 checksum are fetched from the same
resolved release tag. A user-requested downloader update resolves a new tag;
this does not automatically replace an already installed copy.

Upstream distinguishes the licenses of its own source and its release bundles:

- yt-dlp's own repository and Python package code use the **Unlicense**.
- The Windows `yt-dlp.exe` and macOS `yt-dlp_macos` standalone executables bundle
  other projects through PyInstaller; upstream licenses the combined work under
  **GPL-3.0-or-later**, rather than the Unlicense alone.
- The Unix `yt-dlp` zipimport executable also includes third-party JavaScript
  components under the **ISC** and **MIT** licenses.

See the official [release-file licensing notes](https://github.com/yt-dlp/yt-dlp#licensing),
[yt-dlp license](https://github.com/yt-dlp/yt-dlp/blob/master/LICENSE) and
[bundled component notices](https://github.com/yt-dlp/yt-dlp/blob/master/THIRD_PARTY_LICENSES.txt).
When redistributing a downloaded tool, use the licenses, notices and source
requirements corresponding to that tool's release tag, including those of its
bundled components. The application's MIT license does not replace them.

---

## Bundled runtime dependencies

The application ships with the following notable runtime components. These
components use permissive licenses that require their
copyright and permission notices be preserved — which this file does.

| Component | License | Project |
|---|---|---|
| Electron | MIT | <https://github.com/electron/electron> |
| React / React DOM | MIT | <https://github.com/facebook/react> |
| Zustand | MIT | <https://github.com/pmndrs/zustand> |
| Tailwind CSS | MIT | <https://github.com/tailwindlabs/tailwindcss> |
| lucide-react | ISC | <https://github.com/lucide-icons/lucide> |
| music-metadata | MIT | <https://github.com/Borewit/music-metadata> |
| node-id3 | MIT | <https://github.com/Zazama/node-id3> |
| @xhayper/discord-rpc | ISC | <https://github.com/xhayper/discord-rpc> |
| electron-updater | MIT | <https://github.com/electron-userland/electron-builder> |

Electron itself bundles **Chromium** (BSD-3-Clause and numerous other permissive
licenses) and **Node.js** (MIT). The complete license texts for those components
are included inside the Electron distribution (e.g. the `LICENSES.chromium.html`
file shipped with each build).

The MIT and ISC licenses are reproduced below; each named copyright holder above
retains their rights under these terms.

### The MIT License

```
Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

### The ISC License

```
Permission to use, copy, modify, and/or distribute this software for any purpose
with or without fee is hereby granted, provided that the above copyright notice
and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH
REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND
FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT,
INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS
OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF
THIS SOFTWARE.
```

---

*A full machine-readable inventory of every dependency and its license can be
regenerated at any time with a tool such as `license-checker` or
`license-checker-rseidelsohn`.*
