# JON Agent 

This role deploys the JON Agent. It's simple by nature, and just get the agent in place, as well as a configuration file.

## Requirements

TBC.

## Role Variables

```yaml
---
jon_manage_software: true
jon_manage_services: true

jon_agent_repository_url: "http://some/url/"
jon_agent_repository_file: "jon-agent-version.zip"

jon_rhq_configuration:
  # You should actual configuration flags here;
  # These are written to the config file exactly as you see them here.

  RHQ_AGENT_HOME: "/jboss/jon-agent/rhq-agent"
  RHQ_JAVA_HOME: "/usr/java/jdk/"
  RHQ_AGENT_START_COMMAND: "su -m jboss -c '${RHQ_AGENT_HOME}/bin/rhq-agent.sh'"
  RHQ_AGENT_UMASK: 007
  # ...
```

## Dependencies

TBC

## License

MIT

## Author Information

- Michael Crilly
- mike@autologic.cm
