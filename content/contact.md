---
title: "Get in Touch"
description: "Reach out for collaboration, speaking, or just to say hello."
summary: "A privacy-first contact form."
hidemeta: true
showToc: false
---

I'm always open to interesting conversations about distributed systems, engineering culture, or potential collaborations.

<div class="contact-form-container">
<form action="https://api.web3forms.com/submit" method="POST" class="contact-form" id="contact-form">
  <input type="hidden" name="access_key" value="d8aa1c3b-f9ca-44cf-9cf0-8a03eba1d6d9">
  <input type="hidden" name="subject" value="New Contact from aashishkumar.dev">
  <input type="hidden" name="from_name" value="Portfolio Contact Form">
  <input type="checkbox" name="botcheck" class="hidden" style="display: none;">

  <div class="form-group">
    <label for="name">Name</label>
    <input type="text" name="name" id="name" placeholder="Your name" required>
  </div>

  <div class="form-group">
    <label for="email">Email</label>
    <input type="email" name="email" id="email" placeholder="your@email.com" required>
  </div>

  <div class="form-group">
    <label for="subject">Subject</label>
    <input type="text" name="subject" id="subject" placeholder="What's this about?">
  </div>

  <div class="form-group">
    <label for="message">Message</label>
    <textarea name="message" id="message" rows="5" placeholder="Your message..." required></textarea>
  </div>

  <button type="submit" id="submit-btn">Send Message</button>
  <p id="form-status" class="form-status"></p>
</form>
</div>

<div class="contact-social">

**Prefer LinkedIn?** Connect with me at [linkedin.com/in/aashish1412](https://www.linkedin.com/in/aashish1412/).

</div>

<style>
.contact-form-container {
  max-width: 560px;
  margin: 2rem 0;
}

.contact-form .form-group {
  margin-bottom: 1.25rem;
}

.contact-form label {
  display: block;
  margin-bottom: 0.4rem;
  font-weight: 600;
  font-size: 0.9rem;
  letter-spacing: 0.02em;
}

.contact-form input[type="text"],
.contact-form input[type="email"],
.contact-form textarea {
  width: 100%;
  padding: 0.65rem 0.85rem;
  border: 1px solid var(--border);
  border-radius: 6px;
  background: var(--entry);
  color: var(--primary);
  font-family: inherit;
  font-size: 0.95rem;
  transition: border-color 0.2s ease;
  box-sizing: border-box;
}

.contact-form input:focus,
.contact-form textarea:focus {
  outline: none;
  border-color: var(--primary);
}

.contact-form button[type="submit"] {
  padding: 0.7rem 2rem;
  background: var(--primary);
  color: var(--theme);
  border: none;
  border-radius: 6px;
  font-size: 0.95rem;
  font-weight: 600;
  cursor: pointer;
  transition: opacity 0.2s ease;
  letter-spacing: 0.02em;
}

.contact-form button[type="submit"]:hover {
  opacity: 0.85;
}

.form-status {
  margin-top: 1rem;
  font-size: 0.9rem;
}

.contact-social {
  margin-top: 2.5rem;
  padding-top: 1.5rem;
  border-top: 1px solid var(--border);
}
</style>

<script>
const form = document.getElementById('contact-form');
const status = document.getElementById('form-status');
const submitBtn = document.getElementById('submit-btn');

form.addEventListener('submit', async (e) => {
  e.preventDefault();
  const originalText = submitBtn.textContent;
  submitBtn.disabled = true;
  submitBtn.textContent = 'Sending...';
  status.textContent = '';

  const formData = new FormData(form);

  try {
    const response = await fetch('https://api.web3forms.com/submit', {
      method: 'POST',
      body: formData,
    });
    const data = await response.json();

    if (response.ok) {
      status.textContent = '✓ Message sent successfully. I\'ll get back to you soon.';
      status.style.color = '#22c55e';
      form.reset();
    } else {
      status.textContent = '✗ ' + (data.message || 'Something went wrong. Please try again.');
      status.style.color = '#ef4444';
    }
  } catch (err) {
    status.textContent = '✗ Network error. Please try again later.';
    status.style.color = '#ef4444';
  }

  submitBtn.disabled = false;
  submitBtn.textContent = originalText;
});
</script>
