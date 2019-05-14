# Kubernetes chart for Kubebot

[Kubebot](https://github.com/harbur/kubebot) definition (a.k.a Charts) for Kubernetes Helm. For more information about installing and using Helm, see its [README.md](https://github.com/kubernetes/helm/tree/master/README.md). To get a quick introduction to the developer's experience using Helm and Charts see this [developer workflow](https://github.com/kubernetes/helm/blob/master/docs/workflow/developer-workflows.md).

## Kubebot

[Kubebot](https://github.com/harbur/kubebot) is a Kubernetes chatbot for Slack.
## Setup

1. Clone this repository
1. [Create a new bot](https://my.slack.com/services/new/bot) user integration on Slack and get the `token`
1. Update `values.yaml`:
  1. `slack.token` should be the `token` for your bot integration
  1. `slack.admin_nicknames` sould be a list of the nicknames (without `@`) of the users that you want to be able to interact with Kubebot
  1. Set `slack.channel_ids` sould be a list of the channel IDs that you want kubebot to able to interact in. You can get the IDs of your team's channels in `https://slack.com/api/channels.list?token={REPLACE WITH YOUR TOKEN}`
  1. [optional] You can add/remove items from `commands` list to change which commands Kubebot is able to run

## Run

`helm install ./kubebot-chart --name kubebot --namespace kubebot --values values.yaml`