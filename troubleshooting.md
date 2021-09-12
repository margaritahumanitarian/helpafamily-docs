---
description: Tips for anyone having trouble setting up the project
---

# Troubleshooting

## Module Not Found

If you get this error, it probably means you have some dependencies missing. To install them, try:

```
$ yarn
```

{% hint style="info" %}
All dependencies should be listed in package.json, so please submit an issue if you've already tried this.
{% endhint %}

Once you've done that, run the project locally as usual and it should hopefully now work:

```bash
$ yarn dev
```



