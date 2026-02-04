This repository contains the anonymized artifact for our ISSTA 2026 submission, “The Discreet Charm of the Bugeoisie.”

# Dataset Column Descriptions

Anonymity note: To reduce the risk of identifying individuals, we omit certain person-related columns entirely from the released `.csv` file. The Markdown may still describe these omitted columns for transparency.

## Columns Omitted from the Released CSV for Anonymity

The following columns were collected during annotation but are **not included** as columns in the released `.csv` file:

- **reporter_username**: Username of the bug reporter on the tracking platform
- **is_reporter_author_match**: Boolean indicating if the bug reporter is one of the paper authors

## Collection Method

- **Human-annotated**: collected manually by human annotators
- **GitHub API-derived**: obtained automatically using the GitHub API

## Columns (Manual)

- **bug_report_url**: The direct URL to the original bug report
- **closure_reason**: The reason given for closing the issue
- **n_bugs_covered**: The number of distinct bugs described in this single report
- **programming_language**: Programming language of the bug report
- **is_anonymously_reported**: Boolean indicating if the reporter's identity was hidden or anonymous
- **has_repro_steps**: Boolean indicating if the bug report contains explicit text steps to reproduce the issue
- **test_present**: Boolean indicating if a test is included in the bug report or repository
- **fix_entity_type**: Type of entity used to fix the bug (Pull Request or Commit)
- **fix_commit_pr_sha**: The SHA hash of the commit that implemented the fix, if available (e.g., the merge commit for a fixing Pull Request).
- **n_files_changed_in_fix**: The number of files changed in the fix commit or PR
- **fix_component**: Part of the codebase modified to fix the bug
- **is_fail_stop**: Boolean indicating if the bug manifests as a fail-stop error

## Columns (GitHub API)

- **bug_report_url_redirected**: The final resolved URL of the bug report after following any redirects
- **bug_report_title**: The title or summary of the bug report as listed on the tracker
- **created_at**: Timestamp when the bug report was created.
- **status**: The current status of the bug report on the tracker
- **comment_count**: The total number of comments in the issue thread
- **issue_participants_count**: The number of unique users who participated in the issue discussion
- **closed_at**: Timestamp when the issue was closed
- **issue_description_length_chars**: The character count of the initial bug report description
- **issue_first_comment_at**: Timestamp of the first comment posted on the issue
- **pr_head_commit_sha**: The SHA of the head commit for Pull Requests
- **pr_commit_count**: The number of commits included in the Pull Request
- **pr_has_commit_id**: Boolean indicating if the PR is linked to a specific commit ID
- **pr_review_submission_count**: The number of code review submissions received
- **pr_review_rounds_estimate**: An estimate of the number of review rounds
