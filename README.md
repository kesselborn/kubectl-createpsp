# kubectl-createpsp
kubectl plugin to create a simple psp + role + rolebinding as there is no `kubectl create psp …` at the moment.

## Install

Copy `kubectl-createpsp` to a directory which is in your `$PATH` (e.g. `/usr/local/bin`) and make it executable:

```
cp kubectl-createpsp /usr/local/bin
chmod +x /usr/local/bin/kubectl-createpsp
```



## Usage

call

    kubectl createpsp

for the help screen:

```
usage: kubectl-createpsp NAME [SERVICEACCOUNT] [OWNER]

Creates psp, role, rolebinding and (optionally) a service account
for a custom pod security policy

args:
  NAME           name to be used for psp, role and rolebinding (all three will be
                 prefixed with 'psp-' or 'psp:'
  SERVICEACCOUNT allow SERVICEACCOUNT to use this psp -- otherwise
                 a service account with name NAME will be created
  OWNER          if set, add an annotation with owner=OWNER to all resources


```

