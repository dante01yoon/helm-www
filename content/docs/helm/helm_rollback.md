## helm rollback

Rollback a release to a previous revision

### Synopsis


This command rolls back a release to a previous revision.

The first argument of the rollback command is the name of a release, and the
second is a revision (version) number. To see revision numbers, run
'helm history RELEASE'. If you'd like to rollback to the previous release use
'helm rollback [RELEASE] 0'.


```
helm rollback [flags] [RELEASE] [REVISION]
```

### Options

```
      --cleanup-on-fail       Allow deletion of new resources created in this rollback when rollback failed
      --description string    Specify a description for the release
      --dry-run               Simulate a rollback
      --force                 Force resource update through delete/recreate if needed
  -h, --help                  help for rollback
      --no-hooks              Prevent hooks from running during rollback
      --recreate-pods         Performs pods restart for the resource if applicable
      --timeout int           Time in seconds to wait for any individual Kubernetes operation (like Jobs for hooks) (default 300)
      --tls                   Enable TLS for request
      --tls-ca-cert string    Path to TLS CA certificate file (default "$HELM-HOME/ca.pem")
      --tls-cert string       Path to TLS certificate file (default "$HELM-HOME/cert.pem")
      --tls-hostname string   The server name used to verify the hostname on the returned certificates from the server
      --tls-key string        Path to TLS key file (default "$HELM-HOME/key.pem")
      --tls-verify            Enable TLS for request and verify remote
      --wait                  If set, will wait until all Pods, PVCs, Services, and minimum number of Pods of a Deployment are in a ready state before marking the release as successful. It will wait for as long as --timeout
```

### Options inherited from parent commands

```
      --debug                           Enable verbose output
      --home string                     Location of your Helm config. Overrides $HELM-HOME (default "~/.helm")
      --host string                     Address of Tiller. Overrides $HELM-HOST
      --kube-context string             Name of the kubeconfig context to use
      --kubeconfig string               Absolute path of the kubeconfig file to be used
      --tiller-connection-timeout int   The duration (in seconds) Helm will wait to establish a connection to Tiller (default 300)
      --tiller-namespace string         Namespace of Tiller (default "kube-system")
```

### SEE ALSO

* [helm](../../docs/helm/#helm)	 - The Helm package manager for Kubernetes.

###### Auto generated by spf13/cobra on 16-May-2019