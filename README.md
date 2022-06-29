# The simplest WIP blocker ever
Simple Github Action to block PRs with WIP status.

It works by comparing a list of keywords with your PR title and labels, and fails if there's a match (case-insensitive). 

The action takes only one optional parameter: `keywords`.

The default value is: `'wip rfc poc draft'`.

Example usage: 
```yaml
    steps:
      - name: WIP Blocker
        uses: rafaelbeckel/wip-blocker
```

Usage with custom keywords:
```yaml
    steps:
      - name: WIP Blocker
        uses: rafaelbeckel/wip-blocker
        with:
          - keywords: 'wip draft blockme'
```

Example excludind 'rfc poc draft':
```yaml
    steps:
      - name: WIP Blocker
        uses: rafaelbeckel/wip-blocker
        with:
          - keywords: 'wip'
```
