# 26151

Reproduction for [Renovate issue 26151](https://github.com/renovatebot/renovate/discussions/26151#discussioncomment-10020310)

## Current behavior

Renovate creates PRs for Jenkins plugins that do not match the version constraints. It seems to be pulling the latest version regardless of what constraints have been set. For example, the dark-theme plugin requires Jenkins version 2.453.
![image](https://github.com/bsloan-icl/renovate-version-constraint-for-jenkins/assets/85300277/463a3570-2050-4446-86da-3af285229b52)

However, when setting a constraint of <=2.452 in renovate.json, it still creates a PR for the latest version of the dark-theme plugin.


## Expected behavior

Renovate shouldn't be creating PRs for Jenkins plugins that have a "requiredCore" value that doesn't match the constraint.

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/26151#discussioncomment-10020310
