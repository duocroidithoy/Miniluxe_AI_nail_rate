Here is the GitHub `README.md` summary with all icons removed:

---

# AI-Assisted Recruitment for Miniluxe Nail Technicians

A cost-effective system using GPT-4o to pre-screen nail technician applicants through automated photo assessment.

---

## Problem

Miniluxe's traditional recruitment process takes approximately 42 minutes per applicant, leading to wasted time on low-skill candidates:

* 15 low-skill interviews per month = 10.5 hours of wasted time.
* Applicant data comes from ADP, Vonage, and Phone Center.
* In-person interviews and scheduling require significant resources.

---

## Solution: AI-Assisted Skill Assessment

Use GPT-4o to evaluate applicant-submitted nail work before interviews.

### Benefits

* Filters out low-skill candidates
* Saves recruiter time and effort
* Provides fast, objective assessments
* Costs only \~\$5 per 1,000 applicants

---

## System Overview (Racing Metaphor)

| Component | Description                                                                                                      |
| --------- | ---------------------------------------------------------------------------------------------------------------- |
| Track     | Nail photos submitted via [Google Form](https://forms.gle/vcSpMnKfQEeymkhk7)                                     |
| Driver    | GPT-4o model trained to evaluate nail work                                                                       |
| Car       | Python automation script ([Code Repo](https://github.com/duocroidithoy/Miniluxe_AI_nail_rate/blob/main/main.py)) |
| Pit Team  | Human reviewers: Nancy, Donna, Hoang, Hilario, John                                                              |

---

## Data Collection

* Applicants upload photos via a structured form.
* Data flows into [Google Sheet](https://shorturl.at/Aik5Z).
* System detects unrated rows and processes them automatically.

---

## Rating Logic

Each image is scored on:

* Polish Application
* Cuticle Work
* Nail Shape
* Cleanliness

Each attribute is rated 1–10.
Overall Score = average of the four.

| Overall Score | Recommendation            |
| ------------- | ------------------------- |
| ≥ 8.5         | Highly Recommend Hire     |
| ≥ 7           | Recommend Hire            |
| ≥ 5.5         | Further Training Required |
| < 5.5         | Not Recommend Hire        |
| Wrong Format  | All scores = 0, with note |

---

## Testing & Results

Initial testing on 9 valid cases:

* GPT-4o recommendations generally matched human reviewers.
* GPT-4o scored slightly higher on average.
* System accurately flagged incorrectly formatted submissions.

Test results: [Google Sheet](https://shorturl.at/KCIaI)

---

## Technical Notes

* AI outputs may vary slightly each run due to distributed compute clusters.
* Rating Timestamp ensures each row is only processed once.
* Continuous refinement is required for consistency.

---

## Next Steps

### Short-Term

* Collect 50+ valid submissions with both high- and low-skill applicants.
* Enforce photo format compliance for data quality.
* Continue refining rating logic and prompt effectiveness.

### Ethical Considerations

* Disclose AI usage carefully and thoughtfully.
* Protect Miniluxe’s ethical reputation in recruitment.

---

## Takeaways

* Working, scalable prototype is in place.
* System offers significant time and cost savings.
* Continued testing and improvement are required for deployment at scale.

---

## Links

* Google Form: [Submission Form](https://forms.gle/vcSpMnKfQEeymkhk7)
* Google Sheet: [Live Data](https://shorturl.at/Aik5Z)
* Code Repository: [GitHub](https://github.com/duocroidithoy/Miniluxe_AI_nail_rate/blob/main/main.py)
* Test Results: [Analysis Sheet](https://shorturl.at/KCIaI)
