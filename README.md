# Agent's Home 🤖

A demonstration repository showcasing AI-assisted web development using specification-driven methodology with human oversight.

## About This Project

This repository serves as the **home base for an AI coding agent** created as part of the Agentics 101 course. It demonstrates a practical, safety-conscious approach to AI-assisted development where specifications drive implementation and humans maintain quality control.

**Course**: Agentics 101  
**Creators**: Bradley Ross, Nicholas Ruest, The Agentics Foundation  
**AI Assistant**: Claude Sonnet 4.5 (Anthropic)  
**Completed**: December 17, 2025

## Project Overview

**Current Project**: Matt Small's Professional Landing Page

A responsive, accessible landing page showcasing:
- Professional headline and bio
- Credibility badges highlighting expertise in FinOps, Enterprise AI, and Cloud strategy
- Call-to-action button with email integration
- Mobile-first responsive design
- Full WCAG AA accessibility compliance

## Repository Structure

```
agent-home/
├── README.md              # This file - project overview and methodology
├── SAFETY.md             # Agent safety guidelines and operational boundaries
├── spec/                 # Specifications (input for agents) - READ-ONLY
│   ├── README.md         # Specifications folder documentation
│   └── page-spec.md      # Detailed landing page specification
└── src/                  # Source code (output from agents) - AGENT WORKSPACE
    ├── README.md         # Source code folder documentation
    └── index.html        # Generated landing page implementation
```

## Development Approach

### Methodology: Specification-Driven Development

This project follows a **human-supervised, specification-driven approach** to AI-assisted development:

1. **Specifications Define Requirements**
   - Human writes detailed specifications in `spec/` folder
   - Specs include design, functionality, accessibility, and technical requirements
   - Specifications remain read-only to maintain source of truth

2. **Agent Generates Implementation**
   - AI agent (Claude Sonnet 4.5) reads specifications
   - Generates code in `src/` folder based on requirements
   - Follows safety guidelines defined in `SAFETY.md`

3. **Human Reviews and Approves**
   - Every change requires explicit human review
   - Code is tested in browser before committing
   - Human maintains quality control and final decision-making

### Role Definitions

| Role | Responsibilities |
|------|-----------------|
| **Human** | Supervisor, reviewer, quality control, specification author, final decision-maker |
| **Agent** | Code generation, implementation, suggestions, adherence to specifications |

### Safety Model: Human-in-the-Loop (HITL)

All agent operations follow the **Three Laws of Agent Safety**:

1. **Human Approval Required**: Every change needs explicit review
2. **Bounded Scope**: Agent only modifies files in `src/`
3. **Read Before Write**: Agent must see current code before changes

See [`SAFETY.md`](SAFETY.md) for complete safety guidelines.

## Key Features

### Current Implementation

- ✅ **Responsive Design**: Mobile-first approach with breakpoints at 768px and 480px
- ✅ **Accessibility**: WCAG AA compliant with ARIA labels, semantic HTML5, keyboard navigation
- ✅ **Performance**: Single HTML file under 50KB, loads under 3 seconds
- ✅ **Professional Styling**: Custom color scheme (#313357 background, #C0C0C0 text, #ffb900 accents)
- ✅ **Interactive Elements**: Hover effects, focus states, reduced motion support

### Technical Stack

- **HTML5**: Semantic markup
- **CSS3**: Inline styles, flexbox, media queries
- **Accessibility**: ARIA roles, 4.5:1 contrast ratio minimum
- **No Dependencies**: Pure HTML/CSS, no external libraries

## Development Workflow

### Making Changes

1. **Update Specification** (in `spec/page-spec.md`)
   ```markdown
   Add new requirement to specification file
   ```

2. **Agent Generates Code** (in `src/`)
   ```
   Human: "Please implement the updated specification"
   Agent: [Reads spec, generates code, shows changes]
   ```

3. **Human Reviews**
   ```bash
   # Test in browser
   open src/index.html
   
   # Review changes
   git diff src/index.html
   ```

4. **Commit Approved Changes**
   ```bash
   git add src/index.html
   git commit -m "Description of change"
   git push origin main
   ```

### Emergency Recovery

If agent generates problematic code:

1. **Do NOT commit** the changes
2. **If already committed**, use Git history to restore:
   ```bash
   git log --oneline
   git checkout <commit-hash> src/index.html
   ```
3. **Clarify specification** and regenerate
4. **Document** what went wrong to prevent recurrence

## Project Status

| Aspect | Status |
|--------|--------|
| Specification | ✅ Complete and current |
| Implementation | ✅ Matches specification |
| Mobile Responsiveness | ✅ Tested and working |
| Accessibility | ✅ WCAG AA compliant |
| Browser Testing | ✅ Chrome, Firefox, Safari |
| Documentation | ✅ Complete |

## Credits

**Course Development**:
- **Agentics 101** by Bradley Ross, Nicholas Ruest, and The Agentics Foundation
- Course completion: December 17, 2025

**AI Technology**:
- **Claude Sonnet 4.5** by Anthropic
- Used for code generation and implementation assistance

**Methodology**:
- Specification-driven development
- Human-in-the-loop (HITL) safety model
- Bounded agent autonomy with human oversight

## Lessons Learned

1. **Clear Specifications Are Critical**: Detailed specs lead to better implementations
2. **Safety Guidelines Work**: Bounded scope prevents unintended modifications
3. **Human Review Is Essential**: AI assists, but humans maintain quality control
4. **Iterative Development**: Small, reviewed changes are safer than large rewrites
5. **Documentation Matters**: Good docs enable effective human-agent collaboration

## Future Enhancements

Potential improvements for consideration:

- [ ] Add dark/light mode toggle
- [ ] Implement analytics tracking
- [ ] Add animation library for enhanced UX
- [ ] Create additional pages (about, portfolio, contact)
- [ ] Add blog section with RSS feed
- [ ] Implement form handling for contact requests

## License

This project is created for educational purposes as part of the Agentics 101 course.

---

**Note**: This repository demonstrates AI-assisted development with proper safety guardrails and human oversight. It is not intended as a template for fully autonomous AI development, but rather as an example of effective human-AI collaboration in software engineering.