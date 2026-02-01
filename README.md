# ai-jd-resume-matcher
AI-assisted JD and Resume Skill Extraction with Matching Logic to automate resume screening in recruitment workflows.
#src/jd_skill_extractor.py
def extract_jd_skills(jd_text):
    """
    Extracts required skills from Job Description text
    using rule-based and keyword logic.
    """
    jd_text = jd_text.lower()

    known_skills = [
        "python", "sql", "data analysis",
        "apis", "excel", "machine learning"
    ]

    jd_skills = []
    for skill in known_skills:
        if skill in jd_text:
            jd_skills.append(skill)

    return jd_skills
#src/resume_skill_extractor.py
    def extract_resume_skills(resume_text):
    """
    Extracts skills mentioned in resume text.
    """
    resume_text = resume_text.lower()

    known_skills = [
        "python", "sql", "pandas",
        "apis", "java", "excel"
    ]

    resume_skills = []
    for skill in known_skills:
        if skill in resume_text:
            resume_skills.append(skill)

    return resume_skills

#src/matcher.py
    def calculate_match_score(jd_skills, resume_skills):
    """
    Calculates percentage match between JD and Resume skills.
    """
    if not jd_skills:
        return 0

    matched = set(jd_skills).intersection(set(resume_skills))
    score = (len(matched) / len(jd_skills)) * 100

    return round(score, 2)
#data/sample_jd.txt

Role: Python Developer

Required Skills:
Python
SQL
Data Analysis
APIs

Experience: 3+ Years
data/sample_resumes.txt
Candidate:
Skills: Python, SQL, Pandas, APIs
Experience: 4 Years

# AI-Assisted JD & Resume Skill Matching System

## Overview
This project demonstrates how AI-assisted logic can be applied to automate resume screening
by extracting skills from Job Descriptions and candidate resumes.

## Problem Statement
Manual resume screening is time-consuming and inconsistent.
This project automates:
- JD skill extraction
- Resume skill extraction
- Skill matching logic
- Relevance score generation

## Workflow
1. Input Job Description
2. Extract required skills
3. Extract resume skills
4. Match skills and calculate score
5. Output match percentage

## AI & Logic Approach
- Rule-based skill extraction for transparency
- AI-ready design for future semantic enhancements
- Explainable matching logic aligned with ATS systems

## Tools Used
- Python
- GitHub
- Recruitment domain logic

## Output Example
JD Skills: ['python', 'sql', 'data analysis', 'apis']  
Resume Skills: ['python', 'sql', 'pandas', 'apis']  
Match Score: 75%

## Use Case
This system can support recruiters and TA teams by reducing manual screening effort
and improving consistency in shortlisting decisions.

## Future Enhancements
- Integrate Generative AI for semantic skill extraction
- Improve scoring logic using AI similarity
- Extend workflow for interview scheduling




