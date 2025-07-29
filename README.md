# CV Template

This is a LaTeX CV template based on a clean, professional academic CV style. The template includes all the standard sections typically found in academic CVs with generic placeholder content to show the structure and formatting.

## How to Use This Template

### 1. Personal Information
Edit the header section in `cv.tex`:
- Replace `Your Name Here` with your actual name
- Update the address, email, website, and phone information
- Uncomment and modify the job title if desired

### 2. Sections
The CV is organized into sections, each in its own file in the `sections/` directory:

#### Education (`sections/education.tex`)
- Replace university names, locations, and degree information
- Update graduation dates (use `Expected 20XX` for future dates)
- Add or remove entries as needed

#### Research Experience (`sections/research.tex`)
- Replace lab names, institutions, and dates
- Update bullet points to describe your specific research activities
- Use action verbs and quantify achievements where possible
- Add or remove positions as needed

#### Honors & Awards (`sections/awards.tex`)
- Replace award names, organizations, and dates
- Use `\textbf{*~}` to mark declined awards
- Comment out entries you don't want to include

#### Workshops (`sections/workshops.tex`)
- Replace workshop names, hosting institutions, and dates
- Update descriptions to reflect the actual content
- Comment out entries you don't want to include

#### Teaching Experience (`sections/teaching.tex`)
- Replace course numbers, titles, institutions, and semesters
- Update your role (Teaching Assistant, Co-Instructor, Lead Instructor, etc.)
- Add or remove entries as needed

#### Service & Outreach (`sections/service.tex`)
- Replace organization names, positions, and dates
- Update descriptions to reflect your specific activities
- Add or remove entries as needed

#### Conferences & Talks (`sections/presentations.tex`)
- Replace talk titles, conference names, locations, and dates
- Use `\textbf{*~}` for invited talks
- Use `\textbf{$\dagger$~}` for poster presentations
- Add or remove entries as needed

#### Publications (`sections/publications.tex`)
- Replace author names, paper titles, journal names, and dates
- Use `\textbf{*~}` to mark papers where you were a principal author
- Update arXiv numbers and journal information
- Add or remove entries as needed

#### Skills (`sections/skills.tex`)
- Replace skill categories and specific skills with your own
- Organize skills into logical categories
- Add or remove categories as needed

### 3. Compiling
To compile the CV:
```bash
pdflatex cv.tex
```

### 4. Customization Tips
- Keep bullet points concise and impactful
- Use consistent formatting throughout
- Quantify achievements where possible
- Tailor content to your specific field and target audience
- Consider the order of sections based on your priorities

## Template Features
- **Streamlined examples**: Each section shows just enough examples to demonstrate the format
- **Generic content**: Examples are field-agnostic and can be adapted to any discipline
- **Professional formatting**: Clean, academic CV style that works across fields
- **Flexible structure**: Easy to add, remove, or modify sections as needed

## File Structure
```
CV/
├── cv.tex                 # Main CV file
├── cv.sty                 # Style file (don't modify)
├── sections/              # Section files
│   ├── education.tex
│   ├── research.tex
│   ├── awards.tex
│   ├── workshops.tex
│   ├── teaching.tex
│   ├── service.tex
│   ├── presentations.tex
│   ├── publications.tex
│   ├── skills.tex
│   └── interests.tex
└── README_TEMPLATE.md     # This file
```

## Notes
- The style file (`cv.sty`) contains the formatting and should not be modified
- All personal information has been replaced with generic placeholders
- The template maintains the original professional formatting and structure
- You can add or remove sections as needed for your specific use case
- Examples are intentionally generic to work across different academic fields

## GitHub Actions (Optional)

This template includes a GitHub Action that can automatically build your CV and deploy it to your website. The action is disabled by default and requires setup. See `.github/workflows/README.md` for detailed setup instructions. 