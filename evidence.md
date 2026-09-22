**# Class 07: repository, trigger and image evidence**

Use actual output. Replace each blank; do not copy the acceptance text as a result.

**## Step 1 — Create the repository and pipeline**

\- Repository URL:

https://github.com/Chikhl4/AI-Infrastructure-Security-Class-07_Lab

\- Workflow path:

`.github/workflows/ci.yml`

\- First passing run URL and source commit:

https://github.com/Chikhl4/AI-Infrastructure-Security-Class-07_Lab/actions/runs/35755522092

Source commit: `c0101ff`

\- Actual unit-test result:

`5 tests passed; OK`

**## Step 2 — Run only on pushes to main**

\- Commit/run that installed the main-only trigger:

Commit: `9120ec9`

\- \`trigger-check\` branch commit SHA:

`ffa891e`

\- What the Actions page showed for that branch/SHA:

No new Class 07 delivery Actions run was created because its triggered only when push is applied to main branch.

\- Run URL after the same commit was pushed to \`main\`:

https://github.com/Chikhl4/AI-Infrastructure-Security-Class-07_Lab/actions/runs/35757069824

\- Explain why a local commit alone does not start GitHub Actions:

local commit is not by itself push to main branch therefore its doesn't trigger actions.

**## Step 3 — Publish and retrieve the Python image**

\- Package page URL (GHCR, linked to this repository):

https://github.com/Chikhl4/AI-Infrastructure-Security-Class-07_Lab/pkgs/container/ai-infrastructure-security-class-07_lab

\- Source commit, run URL and attempt:

source=3098a620eb4949ec037f26cca5758f5694bc5c64
run=https://github.com/Chikhl4/AI-Infrastructure-Security-Class-07_Lab/actions/runs/35759523671
attempt=1

\- Actual source-test and packaged HTTP test results:

checks=source unit tests + packaged HTTP smoke test passed before publish

\- Complete registry reference (\`repository\@sha256:\` plus 64 hexadecimal digits):

ghcr.io/chikhl4/ai-infrastructure-security-class-07_lab@sha256:b017214cf560063c4fd492f3e632758ead0bf85a53071b066136a916120876f8

\- Platform:

linux/amd64

\- Exact pull command:

docker pull --platform linux/amd64 ghcr.io/chikhl4/ai-infrastructure-security-class-07_lab@sha256:b017214cf560063c4fd492f3e632758ead0bf85a53071b066136a916120876f8

\- Actual pulled-image HTTP test output:

PASS: health + 3 HTTP scoring cases

**## Limits and explanation**

\- One thing these tests do not establish:

hey do not establish that the application is completely secure or free of other errors.

\- Explain the difference between the Git repository and its linked image package:

One contains raw files with code while second is docker image build on those files and code.

\- AI assistance used (tool, task, verification), or \`none\`:

ChatGPT was used to help understand the lab instructions, resolve doubts and work of evidence.md by fixing grammar and extracting all important outputs  from terminal.

**## Optional failure-and-repair extension**

\- Failed commit/run, useful assertion and skipped package job:



\- Repaired commit/run and recovered digest:



Save the successful package job summary, or paste its release record above.

If using a fallback, explicitly mark the uncompleted hosted checks and local

simulation results. Do not invent a repository, run URL or successful GHCR push.
