# Contact form

## Prompt / Question to the AI

i need you to create the contact area for a website. on the left there are 3 text areas for the name, surname, email and subject and on the right the text area. I want it to be extremely simple. i need the css and the html

## AI Plan Response

To create a simple, clean, and responsive contact section, we can use a Flexbox layout. This will keep the inputs on the left and the message area on the right while ensuring they stack neatly on mobile devices.

The HTML Structure
We will group the left-hand inputs into a div and keep the textarea as a sibling for easy alignment.

HTML

<section class="contact-section">
  <form class="contact-form">
    <div class="input-group">
      <input type="text" placeholder="Name" required>
      <input type="text" placeholder="Surname" required>
      <input type="email" placeholder="Email Address" required>
      <input type="text" placeholder="Subject" required>
    </div>

    <div class="message-group">
      <textarea placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </div>

  </form>
</section>
The CSS Styling
This CSS uses a "gap" property to create space between elements and ensures the form takes up the full width of its container.

CSS

/_ Basic Reset _/

- {
  box-sizing: border-box;
  font-family: sans-serif;
  }

.contact-section {
max-width: 900px;
margin: 50px auto;
padding: 20px;
}

.contact-form {
display: flex;
gap: 20px; /_ Space between left and right columns _/
}

/_ Left Column _/
.input-group {
flex: 1;
display: flex;
flex-direction: column;
gap: 15px;
}

/_ Right Column _/
.message-group {
flex: 1;
display: flex;
flex-direction: column;
gap: 15px;
}

/_ Styling Inputs & Textarea _/
input, textarea {
width: 100%;
padding: 12px;
border: 1px solid #ccc;
border-radius: 4px;
font-size: 16px;
}

textarea {
height: 100%; /_ Matches the height of the 4 inputs combined _/
min-height: 200px;
resize: vertical;
}

/_ Submit Button _/
button {
padding: 12px;
background-color: #000;
color: #fff;
border: none;
border-radius: 4px;
cursor: pointer;
transition: opacity 0.2s;
}

button:hover {
opacity: 0.8;
}

/_ Responsive: Stack columns on small screens _/
@media (max-width: 600px) {
.contact-form {
flex-direction: column;
}
}
Key Features of this Design
Minimalist Look: Uses standard borders and a simple black/white color palette.

Flexbox Layout: The flex: 1 property ensures both columns are equal in width.

Responsive: The @media query ensures that on phones, the message box moves below the name/email fields for better readability.

User Experience: Includes :hover states for the button and required attributes for basic validation.

## Implementation Notes

- What was implemented: A new contact form that allows writing.
- What was skipped or changed: I changed the styling.
