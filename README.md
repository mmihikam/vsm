# Value Stream Mapping (VSM) Tool
**Access this tool here: https://mmihikam.github.io/vsm/**
## Table of Contents
1. [About](#About)
2. [What is Value Stream Mapping](#What-is-Value-Stream-Mapping)
3. [What this tool is used for](#What-this-tool-is-used-for)
4. [How to use this tool](#How-to-use-this-tool)
5. [Modification Guide](#Modification-Guide)
   
## About:
This tool lets the user map out a workflow or business process by inputting a sequence of steps, wait times, decisions, and customer touchpoints and instantly generates an interactive visual timeline and metric dashboard. The tool helps users analyze a process to pinpoint exactly where time, effort, or resources are being wasted, and which specific workflows require optimization.

It runs client-side on the chosen web browser using standard HTML, CSS, and vanilla JavaScript. 
It can be opened using the link at the top, or by downloading and opening index.html. Once the interface is open, input process details, and click to generate an instant diagnostic blueprint complete with live lead-time statistics, percentage breakdowns, and analytical issue flags.

## What is Value Stream Mapping
Value Stream Mapping (VSM) is a lean management framework used to analyze, design, and improve the flow of materials and information required to bring a product or service to a customer. It works by:
1. Documenting each component part of an end-to-end process in sequential order, categorizing them into hands-on actions (steps, decisions, communications) or dead time (waits).
2. Measuring time and resource investments for each individual piece (how long a task takes to finish versus how long work sits in a queue waiting to be addressed).
3. Calculating macro process metrics from total durations to evaluate efficiency.
The ultimate goal of Value Stream Mapping is to identify and eliminate waste (activities that add time or cost without adding value to the customer) so that the "Value Stream" becomes as smooth, lean, and fast as possible.

## What this tool is used for
This tool is designed for operational diagnostics, process engineering, and lean transformation initiatives (e.g., standardizing pipelines, uncovering bottlenecks, restructuring touchpoints). It is used to:

* **Inform operational decisions:** Highlight quick-win opportunities for automation, outsourcing, or restructuring prior to implementing costly changes.

* **Visualize workflows smoothly:** Convert a text-based list of administrative tasks into an easy-to-read, horizontal sequence map with standardized, color-coded components.

* **Isolate process waste automatically:** Evaluate data against an analytical rules engine to isolate bottlenecks, extreme cost items, notable delays, and repetitive workflow loops.

## How to use this tool
**1.** Open the interface (https://mmihikam.github.io/vsm/) in any web browser.
**2.** In the "Process name" field, enter the specific title of the workflow you want to map.
**3.** Build the Sequence. Click any of the four template buttons at the bottom to add a new component to your process.
[] Step: Hands-on operational work.
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

