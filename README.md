# Customer-Review-Sentiment-Annotation
A text annotation project where I manually labeled **90 customer reviews** as **Positive**, **Negative** or **Neutral**, following a written set of annotation guidelines.

This is the second project in my data annotation portfolio, followed by a Named Entity Recognition (NER) project and an image annotation project.

---

## Task

For each review, decide the overall sentiment the customer expresses toward their purchase or experience:

| Label | Meaning | Example |
|---|---|---|
| **Positive** | The customer is satisfied or happy | "The customer support team was extremely helpful." |
| **Negative** | The customer is dissatisfied or reports a problem | "My order arrived three days late. Very disappointing." |
| **Neutral** | A factual statement, or no clear satisfaction or dissatisfaction | "I received the package yesterday afternoon." |

---

## Dataset

| Property | Value |
|---|---|
| Reviews | 90 |
| Columns | `Review_id`, `Review_text`, `Sentiment` |
| Labels | Positive, Negative, Neutral |
| Topics | Product quality, delivery, packaging, customer service, pricing, electronics, clothing, food, skincare, books |
| Style | Short factual statements, clear opinions, and longer reviews with mixed or indirect sentiment |

The dataset starts with simple, clear-cut reviews and moves to harder ones: sarcasm, negation, mixed opinions and facts with hidden sentiment.

The Excel file has three sheets: **Customer Reviews** (the data), **Project Summary** and **Annotation Guidelines**.

---

## Annotation Guidelines

1. Label the **overall sentiment** of the whole review, not one word in it.
2. Statements of fact with no opinion ("I ordered two shirts in different sizes") are **Neutral**.
3. A problem the customer reports (late delivery, wrong item, broken product) is **Negative**, even if the wording is calm.
4. Read the **intended meaning**, not the literal words. Sarcasm takes the sentiment it actually expresses.
5. When a review is mixed, label the sentiment the customer **ends on or weighs most**. If the two sides are balanced, use **Neutral**.
6. Negation flips the meaning: "I wouldn't say the fabric is uncomfortable" is not Negative.

Full guidelines are in the *Annotation Guidelines* sheet of the Excel file.

---

## Hard Cases

These reviews tested the guidelines. Each shows the decision I made and why.

| ID | Review | Label | Why |
|---|---|---|---|
| 33 | "Oh great! Another product that stopped working after one day." | Negative | Sarcasm: positive words, negative meaning |
| 45 | "Wonderful! The box was empty, and I paid ₹2,000 for it." | Negative | Sarcasm about a real problem |
| 48 | "If you enjoy waiting forever, this is the delivery service for you." | Negative | Sarcasm: complaint disguised as praise |
| 38 | "Not bad at all! The quality is better than I expected." | Positive | "Not bad" is praise, not criticism |
| 42 | "I expected something terrible after reading the reviews, but this product surprised me." | Positive | Negative words, positive conclusion |
| 31 | "The phone looks beautiful, but the battery barely lasts four hours." | Negative | Mixed review; the complaint outweighs the praise |
| 34 | "The shoes are comfortable, although the colour is slightly different from the pictures." | Positive | Mixed review; the main verdict is positive |
| 40 | "I love the design, hate the material, and I'm still not sure whether I should keep it." | Neutral | Balanced positives and negatives, no verdict |
| 35 | "The customer service representative apologized, but nobody actually solved my problem." | Negative | Polite words, unresolved problem |
| 36 | "I have purchased this brand several times, but this will definitely be my last order." | Negative | Past loyalty, but the final verdict is negative |
| 54 | "I received a refund, so at least the company did the right thing in the end." | Neutral | Problem resolved, but the customer is not happy |
| 59 | "The app asks me to sign in every time I open it. Is that supposed to happen?" | Neutral | A question about behavior, not a clear complaint |
| 52 | "I wouldn't say the fabric is uncomfortable, but it isn't particularly soft either." | Neutral | Double negation, balanced meaning |
| 12 | "The item costs ₹1,500 and comes in three colours." | Neutral | Facts only, no opinion |

---

## Repository Structure

```
comments-review-text-annotation/
├── README.md
├── data/
│   ├── comments_review.xlsx   # reviews + labels + guidelines sheets
│   └── comments_review.csv    # same data, previewable on GitHub
└── docs/
    └── annotation_guidelines.md
```

---

## Skills Demonstrated

- Applying written guidelines consistently across 90 items
- Handling sarcasm, negation and mixed-sentiment text
- Separating factual statements from opinions
- Documenting borderline decisions so another annotator could reproduce them

---

## Next Steps

- [ ] Have a second annotator label the same 90 reviews and report agreement (Cohen's kappa)
- [ ] Review the disagreements and refine the guidelines (v1.1)
- [ ] Add a fourth label such as *Mixed* and compare it with the current rule for balanced reviews

---

## Author

Jonemoni Kalita
linedin- www.linkedin.com/in/jonemoni-kalita-6a56b2234

