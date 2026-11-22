# runner.li

runner.li runs your CI jobs on managed runners operated by [VSHN](https://www.vshn.ch) from Switzerland. It works with GitHub, GitLab and Forgejo.

- **Every job in its own virtual machine.** The machine is deleted when the job ends, so nothing from one job is visible to the next job or to another customer.
- **No runners to operate.** You change one line in your workflow. There is nothing to install, patch or scale on your side.
- **Slots, not minutes.** You pay for a number of jobs that run at the same time, so the bill is the same every month.

runner.li is in a free beta on bare metal in Paris, France. To join, ask for access on [runner.li](https://runner.li).

## Use it with GitHub Actions

1. Install the GitHub App [runner.li CI](https://github.com/apps/runner-li-ci) on the repositories that should use runner.li, not on the whole organization.
2. Send us the installation ID: the number at the end of the installation's settings URL.
3. Set `runs-on` in your workflow to the label we agree on at onboarding.

The steps in full are in the [GitHub guide](https://docs.runner.li/forges/github/).

## What the app can do

| Permission | Why |
| --- | --- |
| Administration: read and write | Register and remove the single-use runner for each job |
| Actions: read | See which jobs are queued |
| Commit statuses: read and write | Show on the commit why a flex job is waiting |
| Metadata: read | Required by GitHub for every app |

GitHub also tells us when a job is queued (the `workflow_job` event), so the job starts without waiting for our next check. No key or token leaves your side.

## Links

- Website: [runner.li](https://runner.li)
- Documentation: [docs.runner.li](https://docs.runner.li)
- Sales: [sales@vshn.ch](mailto:sales@vshn.ch)
- Security reports: [support@vshn.ch](mailto:support@vshn.ch)
