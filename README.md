# Day 7 Git Project

## What is the project?

This is a small production-style repository created to practice Git, GitHub, branches, pull requests, code review, and basic service troubleshooting.

## Project Files

- `app.txt` - Sample application/configuration file.
- `health.txt` - Health check information.
- `status.txt` - Current application status.
- `.gitignore` - Files and directories that should not be committed.

## How do you test it?

Check the application files:

    cat app.txt
    cat health.txt
    cat status.txt

For the health check:

    cat health.txt

Expected result:

    Health check: PASS

## Git Workflow

The workflow used was:

1. Create a feature branch.
2. Make changes to the project.
3. Stage and commit the changes.
4. Push the feature branch to GitHub.
5. Create a Pull Request into `main`.
6. Review the changed files.
7. Merge the Pull Request.
8. Update the local `main` branch using `git pull`.

## Production Challenge

During the production challenge, a local service was tested using `ss` and `curl`.

The listening port was checked first to determine whether the service was running. Then `curl` was used to test the service locally.

When the service was not running, the port was not listening and `curl` could not connect. The root cause was that no service was listening on the expected port. Starting the service fixed the problem.
