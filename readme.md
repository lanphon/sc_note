# SystemC Code Review

This repository contains SystemC library code review and documentation written in AsciiDoc.

## Building Locally

### Prerequisites

1. Install Ruby
2. Install bundler: `gem install bundler`
3. Install Jekyll and dependencies: `bundler install`

### Build

To build the site locally:

```bash
bundle exec jekyll serve
```

Then open `http://localhost:4000` in your browser.

### Build PDF

To build the PDF version (requires CJK font support):

```bash
./build.sh
```

Note: This requires the fonts directory with Chinese fonts for proper rendering.

## GitHub Pages

This repository is configured to automatically build and deploy to GitHub Pages. The site will be published to:
`https://<username>.github.io/<repository>/`

## Content

The documentation covers:
- SystemC QuickThread and coroutine implementation
- SystemC kernel scheduling model
- Events, processes, and primitive channels
- Port, sensitive, and hierarchy
- SystemC trace and synthesis
- TLM 1.0 and TLM 2.0

## License

See LICENSE file for details.