### Repro Steps
- run `pnpm install` @ root of project
- `nx dev app` from root of project
- should see error that buildTarget is required
- now go to packages/app and delete project.json and rename _project.json to project.json
- run `nx dev app` again
- would expect to see `starting app...` from packages/app "dev" script, but given dependency on buildTarget it tries to run the build target which seems should be optional