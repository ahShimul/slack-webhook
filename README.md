
# Notify Slack Action

Send workflow status notifications to Slack.

### Example workflow

```yaml
steps:
  - uses: ahShimul/slack-webhook@master
    if: always()
    with:
      status: ${{ job.status }}
      notify_when: 'failure' # default: 'success,failure,warnings'
    env:
      SLACK_WEBHOOK_URL: ${{ secrets.SLACK_WEBHOOK_URL }} # required
      GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }} # optional
```

