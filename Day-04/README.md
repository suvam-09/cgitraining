# OKR & Product Roadmap Visualization

## Overview
This notebook demonstrates how to visualize Objectives and Key Results (OKRs) and a corresponding product roadmap using Python and its data science libraries. It provides a clear, at-a-glance view of strategic goals, their progress, and the initiatives designed to achieve them, along with their timelines and confidence levels.

## Key Learnings & Takeaways
*   **Structured Goal Setting:** Effective representation of OKRs, including baseline, current, and target values, along with a calculated progress percentage.
*   **Initiative Alignment:** Clear mapping of product initiatives to specific Key Results, providing a direct link between work being done and strategic outcomes.
*   **Visual Progress Tracking:** OKR progress is visualized with color-coded bars, immediately highlighting which Key Results are on track, at risk, or behind.
*   **Interactive Roadmap:** The product roadmap is presented as a Gantt-chart-like visualization, showing initiative durations, and importantly, includes an interactive confidence filter to focus on high-priority or uncertain efforts.

## Applications
This approach can be applied in various organizational contexts for:
*   **Strategic Planning:** Defining and communicating company or team objectives.
*   **Product Management:** Visualizing product roadmaps, managing initiative timelines, and assessing confidence.
*   **Performance Tracking:** Monitoring progress towards key business metrics.
*   **Stakeholder Communication:** Clearly presenting strategic direction and execution status to team members, leadership, and external partners.

## Tools & Tech Stack
*   **Python:** The core programming language.
*   **Pandas:** Used for data manipulation and structuring OKRs and roadmap initiatives into DataFrames.
*   **NumPy:** For numerical operations.
*   **Matplotlib:** The primary library for creating static visualizations (OKR progress bar chart, roadmap timeline).
*   **IPywidgets:** Used to add interactivity, specifically for filtering the roadmap visualization based on initiative confidence.
*   **IPython.display:** For displaying interactive widgets within the notebook environment.

## Extension Tasks Implemented

### Extension Task 1: Adding New Key Results and Initiatives (Attempted and Reverted)
*   **Objective:** To demonstrate how new strategic elements could be dynamically added to the existing OKR and Roadmap frameworks.
*   **Implementation:** Code was generated to `pd.concat` a new Key Result related to "Improve customer satisfaction" and two corresponding initiatives ("Implement 24/7 chat support" and "Personalized onboarding flows") into the respective `okrs` and `roadmap` DataFrames.
*   **Outcome:** This task successfully showed the data integration. However, to maintain focus on the interactive visualization, the DataFrames were subsequently reset to their original state, effectively reverting these additions for the subsequent task.

### Extension Task 2: Implementing an Interactive 'Confidence' Filter for the Roadmap
*   **Objective:** To enhance the roadmap visualization by allowing users to dynamically filter initiatives based on their 'confidence' level (High, Medium, Low).
*   **Implementation Details:**
    1.  **Library Imports:** `ipywidgets` and `IPython.display` were added to the initial setup for interactive functionality.
    2.  **Encapsulated Plotting Logic:** The existing roadmap plotting code was refactored into a Python function, `plot_roadmap`, which takes a `confidence_filter` argument (a list of confidence levels).
    3.  **Interactive Widget:** An `ipywidgets.SelectMultiple` widget was created, providing a multi-select dropdown for users to choose desired confidence levels. It was pre-selected to 'High' to show a default filtered view.
    4.  **Dynamic Visualization:** `ipywidgets.interactive` was used to link the `confidence_selector` widget directly to the `plot_roadmap` function. This setup ensures that every change in the widget's selection automatically triggers an update of the roadmap visualization, displaying only initiatives that match the selected confidence levels.
*   **Impact:** This extension significantly improves the usability of the roadmap, allowing stakeholders to focus on initiatives with specific confidence profiles, which is crucial for risk assessment and strategic decision-making.
