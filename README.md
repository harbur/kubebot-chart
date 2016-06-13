# Kubernetes chart for Kubebot

[Kubebot](https://github.com/harbur/kubebot) definition (a.k.a Charts) for Kubernetes Helm. For more information about installing and using Helm, see its [README.md](https://github.com/kubernetes/helm/tree/master/README.md). To get a quick introduction to the developer's experience using Helm and Charts see this [developer workflow](https://github.com/kubernetes/helm/blob/master/docs/workflow/developer-workflows.md).

## Kubebot

[Kubebot](https://github.com/harbur/kubebot) is a Kubernetes chatbot for Slack.  
## Setup

1. Clone this repository
1. [Create a new bot](https://my.slack.com/services/new/bot) user integration on Slack and get the `token`
1. Update `values.toml`:
  1. set `kubebot_slack_token` with the `token` you got
  2. set `kubebot_slack_admins_nicknames` with the nicknames of the users that you want to be able to interact with Kubebot (use a space as separator)
  3. set `kubebot_slack_channels_ids` with the IDs of the channels you want kubebot to interact (use a space as separator). You can get the ids of your team's channels in `https://slack.com/api/channels.list?token={REPLACE WITH YOUR TOKEN}`. 


## Run

The easiest way to deploy Kubebot to your Kubernetes cluster is using [Tide](https://github.com/harbur/tide):

```
tide up .
```


