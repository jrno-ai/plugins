# Submission contract

Use the connected server's current tool schema if it differs from this reference. `jrno_help` explains the current workflow without receiving the source text.

| Field        | Value                                                                                              |
| ------------ | -------------------------------------------------------------------------------------------------- |
| `sourceId`   | Fresh UUID, reused unchanged for retries of this submission.                                       |
| `name`       | Meaningful prepared title, 1–100 characters.                                                       |
| `summary`    | Concise description of the prepared knowledge, at most 500 characters.                             |
| `content`    | Prepared Markdown text, at most 60,000 characters.                                                 |
| `kind`       | `meeting`, `note`, `research`, or `other`.                                                         |
| `piiReview`  | `redacted` or `none_detected`, reflecting the local review.                                        |
| `sourceUrl`  | Optional supplied public HTTP(S) source URL without secrets or personal identifiers.               |
| `occurredAt` | Optional known event time as an ISO timestamp. Omit when unknown; do not substitute the save time. |

Do not include `userId`, `projectId`, `workspaceId`, credentials, or the uncleaned original. JRNO derives identity and workspace from the OAuth grant.

For large material, select the useful content within the limit or split it into coherent independent submissions when the user's request covers all parts. Do not cut text mid-fact or silently drop decisive caveats. Give each independent item its own UUID.

`jrno_get_submission` accepts `sourceId`. It retrieves a submitted item and processing state; it is not a general search tool. Follow the tool's actual result fields for status and saved-item URL.
