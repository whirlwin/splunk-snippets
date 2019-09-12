splunk-snippets
===============

# 1. Metadata

## 1.1 Finding all indices
    | eventcount summarize=false index=* | dedup index | fields index


## 1.2 Find all sourcetypes
    | metadata type=sourcetypes index=* OR index=_*

## 1.3 Find all hosts
    | metadata type=hosts index=*

## 1.4 Display heaviest logging by k8s Namespace
    index=<my-index> kubernetes.container_name=*** |timechart span=1h count by kubernetes.namespace_name
