# Selflify Preview URL Action

Resolve the final preview URL for a site and optionally wait until that preview is ready.

## What it does

- derives the preview path from the current PR, branch, or tag
- returns the final URL as an output
- optionally waits for either the preview root or the exact deployed commit marker

## Usage

```yaml
- id: preview
  uses: Selflify/preview-url-action@v1
  with:
    site: marketing
    preview-base-domain: example.dev
    wait-mode: exact-sha
```

The final preview URL is available as `${{ steps.preview.outputs.link }}`.
