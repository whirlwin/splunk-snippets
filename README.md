splunk-snippets
===============

# 1. Metadata

## 1.1 Finding all indices

```
| eventcount summarize=false index=* | dedup index | fields index
```
