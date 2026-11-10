---
name: jrno-help
description: Explain how to send notes, ideas, or research to JRNO, how automatic cleanup works, and how to find saved items. Use for onboarding and questions about this plugin.
---

# Using JRNO

Call `jrno_help` for current server capabilities. Call `jrno_workspace` if the user asks which workspace is connected. Neither call needs the content of their notes. If tools are unavailable, explain the setup below without claiming a connection exists.

Connect the MCP URL shown in JRNO under the workspace's data sources. Sign into JRNO in the authorization browser and choose the destination workspace. The connection is bound to that choice. To use a different destination, reconnect and choose it in authorization. Never ask the user to paste a password or OAuth token into chat.

For welcome and general help, lead with this short explanation:

"Send notes, ideas, or research to your JRNO workspace by saying 'Send this to JRNO' and including the material. You can also say 'Save these meeting notes to JRNO' or 'Send our discussion about the launch to JRNO'.

Your assistant automatically selects the useful information, removes chatter and duplication, and reviews the content to remove unnecessary personal details and secrets before sending. It preserves decisions, context, and uncertainty. Only the cleaned content goes to JRNO. You receive a link to the saved item and its processing status. Saved items are shared with your workspace."

Keep onboarding focused on sending. Do not present the identify and clean skills as steps the user needs to perform, ask them what is worth keeping, or list internal tools and review fields. Selection and cleanup are the assistant's job. Mention that users can ask to preview the cleaned content before sending when they want to review it.

Only expand into connection setup, privacy details, or item management when relevant to the user's question. Explain cleanup confidently without promising perfect removal or anonymity. If asked about privacy guarantees, explain that automatic review can miss identifying information. Do not claim the connection exists unless a tool confirms it.

Accepted submissions are processed in the background before becoming searchable. Return the saved-item link to inspect content and status in JRNO. Owners can delete their submissions there. Deletion removes the item from the workspace knowledge lifecycle; it does not remove independent copies or previous assistant conversations. Revoking a connection prevents future calls and leaves saved submissions in place.

Custom installation and public directory publication are different. Do not claim JRNO is listed in a host's public directory. Account plans and organization policy can affect installation. Claude chat custom connectors load MCP tools; they do not automatically install Claude Code plugin skills. Use the supported skill upload/import option when available, or follow the server's help and tool instructions.
