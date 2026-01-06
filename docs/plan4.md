# Contact section background

## Prompt / Question to the AI

i want to add to this section in html <section id="contact" class="section contact">

<div class="container">
<h2 class="section-title animate-on-scroll">Contact us</h2>
<div class="contact-content animate-on-scroll">
<div class="contact-container animate-on-scroll">
<form action="#" method="POST" class="contact-form">
<!-- Left Side: Short Inputs -->
<div class="left-side">
<input type="text" name="name" placeholder="Name" class="input-field" required>
<input type="text" name="surname" placeholder="Surname" class="input-field" required>
<input type="email" name="email" placeholder="Email Address" class="input-field" required>
<input type="text" name="subject" placeholder="Subject" class="input-field" required>
</div>

            <!-- Right Side: Message Area -->
            <div class="right-side">
                <textarea name="message" placeholder="Your message..." class="input-field" required></textarea>
            </div>
        </form>
        </div>

            <a href="mailto:hello@example.com" class="btn btn-primary"
              >Send</a
            >
          </div>
        </div>
      </section> a backround image to the whole background. This is the CSS .contact {

background: var(--color-bg-alt);
text-align: center;
}

## AI Plan Response

To add a background image to that specific section, you'll need to update your CSS to include a background-image property. Since you are using a class and an ID, it is best to target the .contact class or the #contact ID.

Here is the updated CSS and a breakdown of how to make it look professional.

Updated CSS
CSS

.contact {
/_ Use your existing background color as a fallback _/
background-color: var(--color-bg-alt);

/_ Add the image _/
background-image: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('your-image-path.jpg');

/_ Ensure the image covers the whole section _/
background-size: cover;
background-position: center;
background-repeat: no-repeat;

text-align: center;
padding: 80px 0; /_ Adding padding helps the background show more _/
color: #ffffff; /_ Often needed if the background is dark _/
}
Key Properties Explained
background-image: The linear-gradient part adds a subtle dark overlay. This is highly recommended because it makes your white text and form fields much easier to read over a busy image.

background-size: cover: This is the most important line. It ensures the image scales to fill the entire section without stretching or leaving empty gaps.

background-position: center: Keeps the most important part of your image in the middle of the section.

Quick HTML Fix
In your provided HTML, your "Send" button is currently a link (<a>) sitting outside the <form> tag. For a contact form to actually send data, the button should usually be a <button> element inside the form.

Modified HTML Structure:

HTML

<form action="#" method="POST" class="contact-form">
    <div class="left-side">
        </div>
    <div class="right-side">
        <textarea name="message" placeholder="Your message..." class="input-field" required></textarea>
        <button type="submit" class="btn btn-primary">Send</button>
    </div>
</form>
Would you like me to help you write the CSS to make the "Left Side" and "Right Side" of your form sit side-by-side using Flexbox or Grid?

## Implementation Notes

_Brief notes on what was implemented from the plan._

- What was implemented: A background image.
- What was skipped or changed: A few margin and padding modifications.
