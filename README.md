# Value Stream Mapping (VSM) Tool
**Access this tool here: https://mmihikam.github.io/vsm/**
## Table of Contents
1. [About](#About)
2. [What is Value Stream Mapping](#What-Is-Value-Stream-Mapping)
3. [What this tool is used for](#What-This-Tool-Is-Used-For)
4. [How to use this tool](#How-To-Use-This-Tool)
5. [Modification Guide](#Modification-Guide)
   
## About:
This tool lets the user map out a workflow or business process by inputting a sequence of steps, wait times, decisions, and customer touchpoints and instantly generates an interactive visual timeline and metric dashboard. The tool helps users analyze a process to pinpoint exactly where time, effort, or resources are being wasted, and which specific workflows require optimization.

It runs client-side on the chosen web browser using standard HTML, CSS, and vanilla JavaScript. 
It can be opened using the link at the top, or by downloading and opening index.html. Once the interface is open, input process details, and click to generate an instant diagnostic blueprint complete with live lead-time statistics, percentage breakdowns, and analytical issue flags.

## What Is Value Stream Mapping
Value Stream Mapping (VSM) is a lean management framework used to analyze, design, and improve the flow of materials and information required to bring a product or service to a customer. It works by:
1. Documenting each component part of an end-to-end process in sequential order, categorizing them into hands-on actions (steps, decisions, communications) or dead time (waits).
2. Measuring time and resource investments for each individual piece (how long a task takes to finish versus how long work sits in a queue waiting to be addressed).
3. Calculating macro process metrics from total durations to evaluate efficiency.
The ultimate goal of Value Stream Mapping is to identify and eliminate waste (activities that add time or cost without adding value to the customer) so that the "Value Stream" becomes as smooth, lean, and fast as possible.

## What This Tool Is Used For
This tool is designed for operational diagnostics, process engineering, and lean transformation initiatives (e.g., standardizing pipelines, uncovering bottlenecks, restructuring touchpoints). It is used to:

* **Inform operational decisions:** Highlight quick-win opportunities for automation, outsourcing, or restructuring prior to implementing costly changes.

* **Visualize workflows smoothly:** Convert a text-based list of administrative tasks into an easy-to-read, horizontal sequence map with standardized, color-coded components.

* **Isolate process waste automatically:** Evaluate data against an analytical rules engine to isolate bottlenecks, extreme cost items, notable delays, and repetitive workflow loops.

## How To Use This Tool
**1.** Open the interface (https://mmihikam.github.io/vsm/) in any web browser.

**2.** In the "Process name" field, enter the specific title of the workflow you want to map.

**3.** Build the Sequence. Click any of the four template buttons at the bottom to add a new component to your process.
- Step: Hands-on operational work.
- Wait time: Delays, queues, or idle holding periods.
- Decision: Strategic pivot points or approval checkpoints.
- Customer touchpoint: Direct communications or hand-offs sent to/received from a client.
- External Vendor: Tasks, deliverables, or services outsourced to a third-party partner.
- Interdepartmental Handoff: The transfer of data or tasks between different internal teams.
  
**4.** Fill out Component Attributes as you go.
- Name & Details: Provide a concise title and description for the step.
- Duration: Enter the average time it takes.
- People/Roles: Specify the people involved in the step.
- Cost: Select the average cost of the step.
  
**5.** Click "Create Value Stream Map"

**6.** View results by scrolling horizontally to see map and hovering over flags to see problem areas.

**7.** Export by clicking "Print/Save as PDF" and changing settings as desired.

### Additional Elements:
- **Question mark:** Additional guidance.
- **Clear:** Clear all entries.
- **Load Example:** Load a sample process.
- **Trash Can:** Remove an unwanted entry.
- **Up/Down Arrows:** Reorder a step.
- **Edit Details:** Return to input section and edit steps.
- **Flags:** Hover over a flag to read its cause.

**Flagging** 

What gets flagged as a problem area in order of priority:
| Flag | Trigger Condition |
| ---- | ----------------- |
| Biggest bottleneck | Single longest wait node in the entire sequence |
| High vendor cost | External vendor step with high cost |
| Highest cost | Step carrying the highest cost tier |
| Notable delay | Secondary wait periods that account for 20% or more of all wait time |
| Heaviest work step | Work nodes consuming 45% or more of total processing effort |
| Repeated task | Workflow loops where identical step names appear more than once |

## Modification Guide
**IMPORTANT: To avoid accidental alterations create a copy of the html file before making any changes.**
### Project Construction
**Code is located in index.html.** 
To see the code, open index.html in a code editor (e.g. VS Code)

The self contained layout includes:
- **CSS Configurations:** Built with embedded theme variables (:root), full responsive layout classes, flexbox grid structures, and native web @media print rules.
- **UI Rendering Framework:** Built with vanilla JavaScript using dynamic ES6 template literals. It manages screen swaps (input view vs. result view) and saves user cursor focus properties smoothly between state updates.
- **Analytical Logic Engine:** Governs the duration unit calculations, standardizes time metrics to minutes, and runs the conditional loops that output the targeted priority flags.
- **Branding Elements:** Utilizes absolute CSS pseudo-elements (body::before and body::after) to inject background iconography smoothly via raw GitHub CDN paths.
### Suggested AI prompt template for changes
> This project is a self-contained, client-side Value Stream Mapping (VSM) tool built using standard HTML, CSS, and vanilla JavaScript. Please adhere strictly to the following guardrails and architectural principles when modifying the codebase:
>
> Maintain the single-file architecture, keeping all logic, CSS styles, variables, typography, and GitHub CDN branding pseudo-elements intact. Preserve the core state management (state.process) and virtual rendering sync logic without using inline events or scattered event listeners; all user actions must run through high-performance event delegation bound via data-action hooks on the centralized #root wrapper. Any newly injected interactive controls must include proper data-focus-key attributes to avoid breaking real-time cursor tracking during reactive UI updates, and non-report assets should carry the .no-print helper class to ensure executive-ready @media print layouts remain crisp and professional.
>
> Implement the following updates within these parameters:
>
> [Describe specific changes here]

### Publishing changes to existing repository
To publish changes:
1. Log in to GitHub
2. Find the repository you are working in
3. Click the index.html file
4. Click the edit button (pen icon)
5. Make/paste changes
6. Press green "Commit changes" button
7. Changes will automatically be updated on the website

### Creating a new repository
1. If you want one based on another repository:
   - Go to dashboard of the repository you want to clone
   - Click on the green code button
   - Click download zip
   - Open your File Explorer app
   - Right click the zip file you downloaded and click extract all
   - Go to github homepage
   - Click the new button (to create new repository)
   - Fill in details and click create repository
   - Click add file
   - Click upload file
   - Select all the files from the unzipped folder
   - Upload them 

1. If you want a brand new blank repository (ignore if you've already created it):
   - Click the github cat logo at top left (homepage)
   - Click green "New" button at top left
   - Fill out details and click green "Create repository" button

3. Click settings, pages
4. Under branch, change none to main
5. Press save
6. Wait a minute then refresh the page, the link will show up
7. The new page will have the changes, use the new link from now on

*Note: Once a repository is created, the index file can be edited by the owner and the page will automatically update. A new repository only needs to be created if access is not granted to the current one, and changes need to be published.*

Initial Prompt for this tool:

Create an interface where information can be input and a simplified VSM diagram is output. Goals of output: Distinguish between value adding activities and non-value adding activities, Find the root sources of non-value adding activities so that they can be eliminated for faster processes, This tool should be on the macro scale, covering the full process from start to finish. Problem areas (bottlenecks, inefficiencies, etc) should be flagged, so that when you hover over a flag symbol you can see more information about that problem area and how it might be fixed. 
What symbols VSM diagram should include: (have a key with these reworded)

- Step - Something someone does
- Wait time- Nothing is happening, but time is passing
- Decision - Someone has to choose yes/no or approve something
- Problem - Something causes confusion, mistakes, delays, or rework
- Customer communication -  Needs of the customer

Do not use symbols from standard VSM diagrams. The goal is to make this a simple and easy to understand diagram for someone does not know what a VSM is. Use labels to explain what parts are instead of relying on symbols. (The red flag symbol should be used for problem areas though). Since standard symbols aren’t necessary use simple shapes that fit best.
Red flag areas should be done automatically, and should be based on how much time the user has inputted. For example – wherever the majority of the wait time is should be flagged. It should not be the responsibility of the user to identify the red flag areas. That’s the part we are automating.

Formatting:

- How a customer communicates to business
- Process: major steps where work occurs
- Data: underneath each process block – the quantifiable metrics
- Flag points in the flow where improvements are needed
- 
The flow should be from a customer’s perspective. The time ladder in standard VSMs can be confusing, instead focus on the total wait time vs processing time (actual work), and their relation to the total time.
Input section: Before a diagram is filled out the user should be able to input the needed details. Then with all of the details, a vsm diagram can be generated. Details should be editable even after diagram is shown.
The overall goal is for someone who’s never seen a VSM to be able to use this to identify problem areas in their process.

Design: Keep the design professional and sleek and extremely simple. Standard VSMs focus on manufacturing, tailor this one to be able to be more process oriented (for example if there is no physical product in the process, the user can skip a transportation field). Keep a light theme with blues. Only use shades of greyish and light blue, no other colors.
The second window created VSM should have a button to download the created VSM as a pdf. The attached images have some layout structure to follow.

---
###### Built by Mihika Mukherjee
