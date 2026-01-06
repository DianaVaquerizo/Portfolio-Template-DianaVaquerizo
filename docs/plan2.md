# Skill cards

## Prompt / Question to the AI

i want this card to have a different layout, using the same clases and changing the emoji por a small square image. I want the image to be on the left and the right the title on top of the skill bar aligned to the left. Also add two more skills to the grid. 1.The HTMl of the grid is <div class="skills-grid" data-reveal-stagger>

<div class="skill-card">
<span class="skill-icon">🎨</span>
<h3>CSS/Sass</h3>
<div class="skill-bar">
<div class="skill-fill" style="--fill: 95%"></div>
</div>
</div>
<div class="skill-card">
<span class="skill-icon">⚡</span>
<h3>JavaScript</h3>
<div class="skill-bar">
<div class="skill-fill" style="--fill: 90%"></div>
</div>
</div>
<div class="skill-card">
<span class="skill-icon">📱</span>
<h3>Responsive</h3>
<div class="skill-bar">
<div class="skill-fill" style="--fill: 98%"></div>
</div>
</div>
<div class="skill-card">
<span class="skill-icon">♿</span>
<h3>A11y</h3>
<div class="skill-bar">
<div class="skill-fill" style="--fill: 85%"></div>
</div>
</div> 2.The CSS is .skills-grid {
display: grid;
grid-template-columns: repeat(2, 1fr);
gap: var(--space-md);
}

.skill-card {
background: var(--color-bg);
padding: var(--space-md);
border-radius: 12px;
text-align: center;
font-family: var(--font-sans);
font-weight: var(--font-weight-body);
line-height: var(--space-md);
}

## AI Plan Response

To make the .project-card adjust properly to its internal elements (like the image, text, and tags), you need to ensure the card is a flex container. This allows the content to dictate the height of the card while maintaining a clean vertical stack.

Here is the updated CSS including the card and its common internal elements:

CSS

/_ The Card Container _/
.project-card {
background: var(--color-bg-alt);
border-radius: 20px;
overflow: hidden;
transition: transform 0.3s, box-shadow 0.3s;

/_ Adjustment: Auto-height based on content _/
display: flex;
flex-direction: column;
height: 100%; /_ Ensures cards in the same row have equal height _/
}

/_ The Project Image _/
.project-card img {
width: 100%;
aspect-ratio: 16 / 9; /_ Maintains a consistent shape for any image _/
object-fit: cover;
display: block;
}

/_ The Text Content Wrapper _/
.project-content {
padding: var(--space-md);
display: flex;
flex-direction: column;
flex-grow: 1; /_ Pushes footer elements to the bottom if content is short _/
gap: var(--space-xs);
}

.project-card h3 {
font-size: var(--text-lg);
margin: 0;
color: var(--color-text);
}

.project-card p {
font-size: var(--text-sm);
color: var(--color-text-muted);
line-height: 1.6;
margin-bottom: var(--space-sm);
}

/_ Hover effects _/
.project-card:hover {
transform: translateY(-5px);
box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}
Key Improvements:
display: flex & flex-direction: column: This turns the card into a vertical stack. If one card has a longer description than another, the flex layout ensures the card expands to fit the text.

flex-grow: 1 on .project-content: This is a pro-tip. If your cards are in a grid and one card has more text than the others, this property ensures the "bottom" of all cards looks consistent even if the text lengths vary.

aspect-ratio: By setting this on the image, you don't have to manually crop your project screenshots. They will all occupy the same amount of space at the top of the card.

Gap: Instead of using margins on every single element, gap provides a consistent breathing room between the title, the paragraph, and the buttons.

Recommended HTML Structure
To use the CSS above, structure your project card like this:

HTML

<div class="project-card">
  <img src="project-image.jpg" alt="Work Dashboard">
  <div class="project-content">
    <h3>E-commerce Platform</h3>
    <p>A fully responsive dashboard built with React and Node.js featuring real-time analytics.</p>
    </div>
</div>

## Implementation Notes

- What was implemented: A layout change for the skill cards
- What was skipped or changed: The icons, styling and percentages were modified after.
