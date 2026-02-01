# ai-jd-resume-matcher
AI-powered JD–Resume matching system to automate resume screening using LLMs and recruitment workflow logic.

def extract_jd_skills(jd_text):
    """
    Extract skills from Job Description text.
    This is a rule-based approach to keep logic explainable.
    """
    jd_text = jd_text.lower()

    known_skills = [
        "python", "sql", "data analysis", "apis",
        "problem solving", "machine learning", "excel"
    ]

    extracted_skills = []
    for skill in known_skills:
        if skill in jd_text:
            extracted_skills.append(skill)

    return extracted_skills
