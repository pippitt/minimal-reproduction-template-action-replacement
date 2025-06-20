## Current behavior

PR to replace action `gradle/gradle-build-action` with `gradle/actions/setup-gradle` fails with error on `depName mismatch`
Seems to be from https://github.com/renovatebot/renovate/blob/main/lib/workers/repository/update/branch/auto-replace.ts#L62-L76

Looking at the logs, the newDepName is being truncated to "gradle/actions" instead of "gradle/actions/setup-gradle"

## Expected behavior

PR to replace action would be created. 
Did base work on https://github.com/renovatebot/renovate/blob/main/lib/data/replacements.json#L674-L685, so this preset is probably also broken

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/36634
