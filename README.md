# Job Application Crew README

This repository contains a suite of AI agents designed to help job applicants prepare for job applications, from researching job postings to tailoring resumes, and preparing for interviews. The agents and tools are built using the `crewai` framework, integrated with various resources to streamline the job application process.

## Purpose
The purpose of this project is to guide job applicants through the process of preparing and submitting their applications. The crew of agents takes input, processes information, and generates job application materials such as a tailored resume and interview preparation content.

### Features:
- **Job Research**: Analyze job postings to identify key skills, qualifications, and requirements.
- **Personal Profiling**: Create a detailed personal and professional profile from GitHub URLs and personal write-ups.
- **Resume Strategy**: Tailor a resume to best match a job posting based on research and profiling.
- **Interview Preparation**: Generate interview questions and talking points based on the tailored resume and job requirements.

## How It Works

### Agents
1. **Researcher (Tech Job Researcher)**: This agent analyzes job postings to extract key skills, qualifications, and experience required by the employer.
2. **Profiler (Personal Profiler for Engineers)**: This agent collects and synthesizes information from a candidate's GitHub URL and personal write-up to build a comprehensive profile.
3. **Resume Strategist (Resume Strategist for Engineers)**: This agent takes the job posting research and candidate profile to refine and enhance the resume.
4. **Interview Preparer (Engineering Interview Preparer)**: This agent generates a set of interview questions and talking points to help candidates prepare for the interview based on their tailored resume and job requirements.

### Tools
- **ScrapeWebsiteTool**: Extracts information from websites.
- **SerperDevTool**: Performs internet searches to gather job-related information.
- **FileReadTool**: Reads files (e.g., resumes) to extract relevant information.
- **PDFSearchTool**: Searches and processes PDF documents for specific information.

### Tasks
1. **Research Task**: Extracts and categorizes key job requirements from a job posting URL.
2. **Profile Task**: Creates a personal and professional profile based on the candidate’s GitHub URL and personal write-up.
3. **Resume Strategy Task**: Tailors the resume by highlighting the most relevant skills and experience.
4. **Interview Preparation Task**: Generates interview questions and talking points to help candidates prepare.

### Workflow
1. The **Researcher** analyzes the job posting and identifies the key skills and qualifications.
2. The **Profiler** builds a profile using the candidate’s GitHub URL and personal write-up.
3. The **Resume Strategist** refines and updates the resume to match the job posting.
4. The **Interview Preparer** creates interview materials to help the candidate prepare for the interview.

## Requirements
- **Python 3.7+**
- **crewai==0.28.8**
- **crewai_tools==0.1.6**
- **langchain_community==0.0.2**
- **embedchain==0.1.125**
- **google-generativeai**

## Installation

To install the necessary dependencies, run:

```bash
pip install crewai==0.28.8 crewai_tools==0.1.6 langchain_community==0.0.2
pip install embedchain google-generativeai
```

## Usage

1. **Create Inputs**: Set the values for `job_posting_url`, `github_url`, and `personal_writeup` in the `job_application_inputs` dictionary.
   ```python
   job_application_inputs = {
       'job_posting_url': 'https://example.com/job-posting',
       'github_url': 'https://github.com/user',
       'personal_writeup': 'A budding software engineer with a good combination of development skills.'
   }
   ```

2. **Kick Off the Crew**: Initiate the job application workflow.
   ```python
   result = job_application_crew.kickoff(inputs=job_application_inputs)
   ```

3. **Output**: The tasks will generate the following outputs:
   - **Tailored Resume**: A markdown file (`tailored_resume.md`) highlighting the most relevant qualifications and experience.
   - **Interview Materials**: A markdown file (`interview_materials.md`) containing interview questions and talking points.

## Backstory
Each agent has a specific role to ensure that the job application materials are the best possible:
- **Researcher**: Expert in extracting key job requirements.
- **Profiler**: Analyzes personal and professional profiles to ensure the resume stands out.
- **Resume Strategist**: Specializes in refining resumes to match job postings.
- **Interview Preparer**: Prepares candidates for interviews with relevant questions and talking points.

## Conclusion
This project provides a comprehensive toolkit to help job applicants succeed by analyzing job postings, creating tailored resumes, and preparing for interviews. The integration of multiple agents and tools ensures a thorough approach to job application preparation.

