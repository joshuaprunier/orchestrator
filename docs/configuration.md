# Configuration

Documenting and explaining all configuration variables turns to be a daunting task, as goes as deep as explain-the-code-in-words. There is an ongoing effort in pruning and simplifying the configuration.

The de-facto configuration list is located in [config.go](https://github.com/github/orchestrator/blob/master/go/config/config.go).

You are undoubtedly interested in configuring some basic components: the backend database, hosts discoveries. You may choose to use Pseudo-GTID. You may want `orchestrator` to notify upon failure, or you may wish to run full blown automated recovery.

Use the following small steps to configure `orchestrator`:

- [Backend](configuration-backend.md)
- [Discovery: basic](configuration-discovery-basic.md)
- [Discovery: resolving names](configuration-discovery-resolve.md)
- [Discovery: classifying servers](configuration-discovery-classifying.md)
- [Discovery: Pseudo-GTID](configuration-discovery-pseudo-gtid.md)
- [Failure detection](configuration-failure-detection.md)
- [Recovery](configuration-recovery.md)
- Security: See [security](#security) section.
