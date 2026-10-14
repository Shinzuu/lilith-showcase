Set up Lilith, a local chief-of-staff dashboard built on Claude Code, on this computer. Do as much as you can yourself and ask me only for the things you cannot do.

<context>
Lilith is a personal service. It polls my work sources (a task board, chat, email, meeting notes, calendar and my running Claude Code sessions), sorts every item by client, and shows one local web page that answers "what needs me now?". It was built for one Linux laptop, so expect to adapt it. I received the Lilith folder from its author; it is not downloaded from anywhere. The folder's README describes installation and configuration; read it first and follow it. Where it and this prompt disagree, the README wins.

What Lilith needs:
- Linux with systemd user services.
- Node.js 26 or later (it runs its TypeScript sources directly, no build step).
- Claude Code, logged in with my own account. Lilith calls it as its only reader of raw text.
- Optional sources, each with my own login: a chat tool, an email tool, a task board client, and meeting-notes and calendar connectors. Any of them can stay off.
- Two config files: one for my names and sources, one for my clients and the words that identify them.
</context>

<steps>
1. Ask me where the Lilith folder is. Confirm it is the right folder by finding its README and test suite. Do not edit anything in it yet.
2. Check this machine: Linux, systemd user services, Node.js version, Claude Code login. Tell me in one short list what is missing.
3. Install the dependencies and run the project's own checks (typecheck and tests). Report the result. Stop if tests fail.
4. Run the installer in its dry-run mode first and show me exactly what it would create or change. Run it for real only after I say yes.
5. Help me fill in the two config files: my names and addresses, which sources to turn on, and my clients with their match words. Ask me for each value. Never put a token, password or API key in these files; each source uses its own tool's login.
6. Start the service. Leave polling off. Tell me how to open the page and that I press On when I am ready.
7. Report what you installed, what the checks said, which sources are on, and anything still open.
</steps>

<rules>
- Do not turn polling on, send any message, or enable backups or alerts. I do those myself.
- Never read, print or copy any credential file of the source tools.
- If a step fails twice, stop and tell me what you saw instead of trying other routes.
</rules>
