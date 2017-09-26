splunk-snippets
===============

# 1. Metadata

## 1.1 Finding all indices

    | eventcount summarize=false index=* | dedup index | fields index


## 1.1 Find all sourcetypes
    | metadata type=sourcetypes index=* OR index=_*
