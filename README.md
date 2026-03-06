# Execution
`ansible-playbook bootstrapper.yml`

# Variables
| Variable | Description |
| -------- | ----------- |
| `ocp_api` | URL for the OpenShift API, ex: `https://api.openshift.cluster.api.com:6443` |
| `ocp_token` | Login token, ex: `sha256~asdfjklasdfjlkasdjflk` |
| `ocp_cluster_name` | OpenShift Cluster Name, ex: `cluster-f29bc` |
| `ocp_base_domain` | OpenShift Cluster Domain, ex: `f29bc.sandbox2320.opentlc.com` |

# Description
`bootstrapper.yml` calls tasks files that create the Namespaces, OperatorGroups, Operators, and other various resources required to bootstrap the argocd-agent. The resources are located in the respective folders and applied as rendered Jinja templates (even though some are not templates).