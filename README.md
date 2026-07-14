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
| Highest cost | Step carrying the highest cost tier |
| Notable delay | Secondary wait periods that account for 20% or more of all wait time |
| Heaviest work step | Work nodes consuming 45% or more of total processing effort |
| Repeated task | Workflow loops where identical step names appear more than once |

## Modification Guide
**IMPORTANT: To avoid accidental alterations create a copy of the html file before making any changes.**
### Project Construction
**Code is located in index.html.** The self contained layout includes:
- **CSS Configurations:** Built with embedded theme variables (:root), full responsive layout classes, flexbox grid structures, and native web @media print rules.
- **UI Rendering Framework:** Built with vanilla JavaScript using dynamic ES6 template literals. It manages screen swaps (input view vs. result view) and saves user cursor focus properties smoothly between state updates.
- **Analytical Logic Engine:** Governs the duration unit calculations, standardizes time metrics to minutes, and runs the conditional loops that output the targeted priority flags.
- **Branding Elements:** Utilizes absolute CSS pseudo-elements (body::before and body::after) to inject background iconography smoothly via raw GitHub CDN paths.
### Suggested AI prompt template for changes
This project is a self-contained, client-side Value Stream Mapping (VSM) tool built using standard HTML, CSS, and vanilla JavaScript. Please adhere strictly to the following guardrails and architectural principles when modifying the codebase:

CODE FORMAT & ARCHITECTURE: Maintain the single-file architecture. Do not split the code into separate external files or break out the logic. Preserve the existing state management object structure (`state.process`) and virtual rendering synchronization logic. VISUAL THEME & LAYOUTS: Do not modify, remove, or alter any CSS styles, variables, typography, padding scales, or structural color codes unless explicitly asked to do so. Ensure that the CSS absolute pseudo-elements (`body::before` and `body::after`) pointing to branding assets on the GitHub CDN remain untouched. PRINT FUNCTIONALITY: Ensure any added fields, temporary state indicators, or interactive configurations are properly tagged with the `.no-print` helper class if they are not meant to appear on final PDF or physical report exports. Do not break the current `@media print` layouts that optimize the flow of the results dashboard view. EVEN DELEGATION & RE-RENDERING: The app relies strictly on high-performance event delegation. All actions and input listeners are bound directly to the centralized `#root` wrapper using `data-action` hooks. Do not switch to inline event attributes (like onclick/oninput) or manual `addEventListener` attachments scattered through the DOM string literals. Maintain the centralized state management and reactive trigger flow.

Implement the following updates within these parameters:
[Describe specific changes here]
