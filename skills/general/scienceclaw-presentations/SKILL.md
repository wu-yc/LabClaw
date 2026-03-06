# ScienceClaw Presentations — Joey's PPT Templates

Joey's reference for all presentation work. Use this skill when creating academic presentations.

---

## Templates

### Group Meeting

- **Use**: Informal lab meeting / group meeting
- **Sections**: Title, Background, Methods, Results, Next Steps, Questions
- **Style**: Clean, minimal, data-focused
- **Slide count**: 10-15
- **Tone**: Conversational but structured

### Thesis Defense

- **Use**: PhD/Master thesis defense
- **Sections**: Title, Committee, Background, Aims, Methods, Results (by aim), Discussion, Conclusions, Future Work, Acknowledgments, Questions
- **Style**: Formal, comprehensive, narrative arc
- **Slide count**: 30-50
- **Tone**: Authoritative, builds from problem to contribution

### Conference Talk

- **Use**: Conference oral presentation (10-15 min)
- **Sections**: Title, Motivation, Key Question, Approach, Results (3-5 key), Impact, Acknowledgments
- **Style**: Punchy, one-message-per-slide, builds to climax
- **Slide count**: 12-20
- **Tone**: Engaging, clear takeaways, audience-first

### Poster

- **Use**: Academic poster (48x36 inches typical)
- **Sections**: Title/Authors, Background, Methods, Results, Conclusions, References, QR Code
- **Style**: Visual hierarchy, scannable at 2 meters
- **Slide count**: 1 (poster layout)
- **Tone**: Concise, conversation-starter

---

## Slide Design Principles

1. **One message per slide**. If a slide needs two points, it needs two slides.
2. **Build narrative tension**. Motivation → Question → Approach → Discovery → Impact.
3. **Visuals over text**. A figure with a one-line title beats three bullet points.
4. **Audience calibration**. Group meeting: peers who know the jargon. Conference: mixed audience. Defense: experts who will probe.
5. **Timing**: ~1 minute per slide for talks, ~2 minutes per poster section for conversations.

---

## python-pptx Code Patterns

When generating .pptx files via the Compute Server:

```python
from pptx import Presentation
from pptx.util import Inches, Pt
from pptx.enum.text import PP_ALIGN

prs = Presentation()
prs.slide_width = Inches(13.333)
prs.slide_height = Inches(7.5)

# Title slide
slide = prs.slides.add_slide(prs.slide_layouts[0])
slide.shapes.title.text = "Title Here"
slide.placeholders[1].text = "Author | Affiliation | Date"

# Content slide with figure
slide = prs.slides.add_slide(prs.slide_layouts[5])  # blank
slide.shapes.add_picture("figure.png", Inches(1), Inches(1.5), width=Inches(11))

prs.save("output.pptx")
```

---

## Reference Formatting

Presentations should cite key references in footer text (Author et al., Year) with full references on the last slide. Use Vancouver/numbered style for dense slides, Author-Year for sparse slides.
