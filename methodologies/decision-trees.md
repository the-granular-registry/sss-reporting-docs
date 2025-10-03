# SSS Designation Decision Trees

## Monopoly supplier or facilities with regulated cost recovery

\{% @mermaid/diagram content="flowchart TB A\["Is the resource part of default service for all customers?"] -- Yes --> B\["Standard Supply Service\
Option to claim up to your\
pro rata share"] A -- No --> C\["Is the resource part of a green tariff or\
other specified product?"] C -- Yes --> D\["Are all costs recovered through rates paid\
by subscribers to the specified product\
(e.g., green tariff)?"] C -- No --> B D -- Yes --> F\["Was the resource initially built to serve\
the specified product?"] D -- No --> B F -- Yes --> E\["Not SSS\
Eligible for preferential claims without limitation"] F -- No --> B %% ───────────── Styling (optional) ────── style B fill:#e6fff9,stroke:#e6fff9,stroke-width:1.5px style E fill:#ffe6ec,stroke:#ffe6ec,stroke-width:1.5px

" %\}

## Policy Mandates / Compliance Programs

\{% @mermaid/diagram content="graph TD Q1\["Does the resource participate in a\
mandatory clean energy program required\
by legislation or regulation?"] -->|Yes| Q2\["Is the certificate retired or made ineligible\
by participation in the program?"] Q1 -->|No| End\["Not SSS\
Eligible for preferential claims\
beyond SSS allocation"] Q2 -->|Yes| Q3\["Are the costs for this program being\
recovered through the utility bill or\
supplier contract?"] Q2 -->|No| End Q3 -->|Yes| SSS\["Standard Supply Service\
Option to claim up to your pro rata share"] Q3 -->|No| End

```
    %% ───────────── Styling (optional) ──────
style SSS fill:#e6fff9,stroke:#e6fff9,stroke-width:1.5px
style End fill:#ffe6ec,stroke:#ffe6ec,stroke-width:1.5px" %}
```

## Publicly owned

\{% @mermaid/diagram content="graph TD Q1\["Is the resource majority owned by a\
government entity supplying load in their\
home country or region?"] -->|Yes| Q2\["Is the resource taxpayer funded?"] Q1 -->|No| End\["Not SSS\
Eligible for preferential claims beyond SSS allocation"] Q2 -->|Yes| Q3\["Was the resource developed through a\
project awarded through competitive\
process where government-owned\
companies receive no taxpayer support\
different from what a privately owned\
company would receive?"] Q2 -->|No| End Q3 -->|Yes| End Q3 -->|No| SSS\["Standard Supply Service\
Option to claim up to your pro rata share"]

```
    %% ───────────── Styling (optional) ──────
style SSS fill:#e6fff9,stroke:#e6fff9,stroke-width:1.5px
style End fill:#ffe6ec,stroke:#ffe6ec,stroke-width:1.5px" %}
```
