# Servers and Endpoints

## Who is responsible for patching a system in account/zone/tier/layer/VPC/SG?

```j1ql
// Returns the owner of hosts in a particular account
Find Host with tag.AccountName = '{AccountName}' as h
  return h.displayName, h.owner

// Returns the owner of images used by hosts in a particular account
Find Host with tag.AccountName = '{AccountName}' as h
  that uses Image as i
  return h.displayName, h.owner, i.displayName, i.owner
```