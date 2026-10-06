 application projects
Two small, tested services that mirror ClearFeed's product: Slack-native support ticketing and an AI support agent.
project	what it is
`threaddesk/`	Slack ↔ GitHub ticketing: AI triage, two-way sync, SLA tracking, outbox with retries (29 tests)
`supportpilot/`	RAG support agent: cited answers, confidence-gated handoff, approval-gated actions, eval harness (35 tests)
`python e2e_demo.py` runs both together with all external services faked: Slack mention → agent proposes a ticket → human
approves → ThreadDesk creates it and a GitHub issue → GitHub webhook closes it → agent reports the status.
Neither project has been run against live Slack, GitHub or the Anthropic API; those calls are covered by mocked tests. Read each README's "Known limitations" before describing them on a resume.
