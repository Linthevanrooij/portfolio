---
layout: default
title: Contact
---

**About me**  

Hi there! 

I am Linthe van Rooij, currently finishing my graduation project from Creative Intelligence and Technology (CRIT).

Check out some of the projects I created during my Master's CRIT, a program that allowed me to establish a foundation in technology and blend it with my artistic/creative side. The projects focus mostly on interactive participation, often together with a playful twist. 

<fieldset>
  <form id="contact-form">
    <h2>Let's get in touch</h2>

    <p>
      <label for="name">Name:</label>
      <input type="text" id="name" name="Name" required />
    </p>

    <p>
      <label for="company">Company:</label>
      <input type="text" id="company" name="Company" />
    </p>

    <p>
      <label for="message">Message:</label>
      <textarea id="message" name="Message" rows="10" cols="40" required></textarea>
    </p>

    <p>
      <button type="submit">Submit</button>
    </p>
  </form>
</fieldset>

<script>
  document.getElementById('contact-form').addEventListener('submit', function (e) {
    e.preventDefault(); // Prevent actual form submission

    const name = document.getElementById('name').value.trim();
    const company = document.getElementById('company').value.trim();
    const message = document.getElementById('message').value.trim();

    const subject = `New message from ${name}${company ? ', ' + company : ''}`;
    
    const mailtoLink = `mailto:linthe.vr@live.nl?subject=${encodeURIComponent(subject)}`;

    window.location.href = mailtoLink;
  });
</script>
