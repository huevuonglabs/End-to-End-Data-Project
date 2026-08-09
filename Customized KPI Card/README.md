How I Built a Custom KPI Card Viz Extension with Claude Code

KPI cards for dashboards used to take almost a full day to design: pulling metrics, multiple calculation fields, formatting, laying out. The process is time-consuming, and discouraged me whenever design new dashboard with new dataset.

So I built a Claude-powered Tableau Viz Extension that generates KPI cards straight from source data. A day's work now takes minutes.

Here's how:

1. Prompt in plain language

. Point Claude at a sample if you have one:

"I've uploaded kpi_template.twbx. Analyze the KPI banner design — layout, fonts, colors, calculated fields — and draft a PRD for a reusable Tableau Viz Extension that replicates it."

No sample? Ask Claude to design one from scratch, that works fine too.

2. Get the files. Claude generates a PRD plus the extension itself: .html, .json, .css, and a .trex file (the Tableau manifest).

3. Load into Tableau. Drag the .trex file into Viz Extension → Access Local Viz Extension.



4. Iterate. Keep refining with follow-up prompts until the design's right.

5. Add a settings panel. Have Claude build a settings button so you can tweak formatting yourself later.



6. Host it. File .trex runs on localhost by default and only visible to you. To share, publish it somewhere accessible. I used Tableau Ops to upload file and download the new .trex file, about a minute. https://ext.tableauops.com/

Note: I did the whole process on the free version of Claude, so no need to worry about subscriptions to try it yourself.

Key insight

That kind of repetitive, well-defined transformation is exactly what an AI coding assistant can reliably automate. This approach also helps standardize KPI cards, making them more consistent across dashboards and teams.

 
