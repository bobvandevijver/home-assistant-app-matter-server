# Release documentation for developers

## Matter Server Update Procedure

When updating the server library in the app (formerly known as add-on) follow these steps:

1. Update the `matterjs-server` image tag in the `BUILD_FROM` default in `Dockerfile`.
2. If the minimal supported schema version has changed, set the `homeassistant` key in `config.yaml` to the minimum version of Home Assistant Core required to install or update the app.
3. Publish a GitHub release. Its tag sets the app version. Bump to a new major version if the minimum schema version has changed.
4. Include a markdown link to the GitHub release of the server in the release notes. These release notes will be copied to the full changelog in the `home-assistant/apps` repository.
