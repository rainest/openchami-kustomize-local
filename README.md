# openchami-kustomize-local

This is an example overlay Kustomization for the OpenCHAMI Kustomize manifests.
It deploys generic components and adds password Secrets for them.

To configure your instance, edit `remote/services/kustomization.yaml` and
`remote/test-node/userdata` and replace the `CHANGEME` strings to your
passwords and SSH keys.

These passwords are plaintext and not secure for production use. The overlay is
provided for convencience to simplify the creation of test environments.

Per https://argo-cd.readthedocs.io/en/stable/operator-manual/secret-management/
you should instead create these Secrets manually for a production environment.

I'd like to eventually explore either https://github.com/viaduct-ai/kustomize-sops
or https://github.com/bitnami-labs/sealed-secrets as a means of provisioning
secure environments without manual Secret management.
