# JON Agent 

This role deploys the JON Agent. It's simple by nature, and just get the agent in place, as well as a configuration file.

## Version

0.2.0

## Requirements

- JON requires a JVM. I've tested the OpenJDK 1.7.1 as working on CentOS 6.6;
- A "jboss" user should be created, but this is configurable incase your environment is different;
- You'll have to provide a JON archive your self, from RedHat;

## Role Variables

```yaml
---
autologic_jon_manage_software: true
autologic_jon_manage_service: true
autologic_jon_manage_configuration: true
autologic_jon_manage_user: true

autologic_jon_agent_repository_url: "http://some/url/"
autologic_jon_agent_repository_file: "jon-agent.tar.gz"
autologic_jon_agent_extract_to_path: "/jon-agent"

autologic_jon_username: "jboss"
autologic_jon_username_uid: "5000"

autologic_jon_service_name: "rhq-agent-wrapper"
autologic_jon_rhq_configuration: False
```

### Notes

- The ```username_uid``` flag is there as some people like to keep UIDs consistent across their estate.

## Dependencies

TBC

## License

MIT

## Author Information

- Michael Crilly
- mike@autologic.cm
