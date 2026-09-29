# Mission AI wake-up

One hourly workflow wakes the existing Mission AI test service on Render's Free runtime. It performs a single unauthenticated GET with a bounded timeout and no retry loop.

This repository contains no credentials, database settings, task contents or conversation history. It makes no AI provider request and does not change the original chat service. Native scheduler integration and accounting acceptance are separate requirements; a successful wake-up does not prove tasks are enabled or completed.

Scheduling is best effort: GitHub can delay scheduled workflows or disable schedules after extended repository inactivity. Local computer tasks still require an awake Mac and human authorization.

Only standard GitHub-hosted public-repository runners are used. No paid runner or new Render resource is provisioned.
