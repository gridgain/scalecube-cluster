# Release

Publishing is done manually to GridGain Nexus (`maven.gridgain.com`).

1. Set the version:
   ```bash
   mvn versions:set -DnewVersion=release-2.7.7-java11 -DgenerateBackupPoms=false
   ```
2. Deploy:
   ```bash
   mvn --batch-mode deploy -DskipTests
   ```

Make sure your local `~/.m2/settings.xml` contains credentials for the
`external` server that are allowed to publish.
