# Medical Outreach Campaign using CrewAI

This project uses [CrewAI](https://docs.crewai.com/) to promote medical solutions (e.g., devices, treatments) to healthcare institutions like hospitals or clinics by profiling them and crafting personalized outreach for decision-makers.

## Overview
- **Purpose**: Target healthcare institutions with tailored medical solution proposals.
- **Focus**: Adapted from a sales campaign to a medical context, with the same structure.

## Agents
- **Medical Sales Specialist**: Profiles healthcare institutions to identify needs and decision-makers.
- **Medical Outreach Coordinator**: Creates personalized communications for medical professionals.

## Tasks
- **Lead Profiling Task**: Gathers data on an institution (e.g., Cleveland Clinic) and suggests solution benefits.
- **Personalized Outreach Task**: Drafts professional, patient-care-focused messages for decision-makers.

## Tools
- **DirectoryReadTool**: Reads medical guidelines or specs.
- **FileReadTool**: Accesses files like clinical data.
- **SerperDevTool**: Searches for institution details online.
- **SentimentAnalysisTool**: Ensures positive messaging.

## How to Run
1. **Set up API keys**: Add OpenAI and Serper API keys in `utils.py`.
2. **Define inputs**:
   ```python
   inputs = {
       "lead_name": "Chagua Health",
       "industry": "Healthcare",
       "key_decision_maker": "Dr Koech",
       "position": "CEO",
       "milestone": "new cardiac care center"
   }
   ```
3. **Run it**: Use `result = crew.kickoff(inputs=inputs)` and view with `Markdown(result)`.

