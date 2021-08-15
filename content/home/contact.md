+++
# Contact widget.
widget = "contact"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 130  # Order that this section will appear.

title = "Contact"
subtitle = ""

[design.background]
# color = 'floralwhite'

# Automatically link email and phone?
autolink = true

# Email form provider
#   0: Disable email form
#   1: Netlify (requires that the site is hosted by Netlify)
#   2: formspree.io
email_form = 2

# Netlify form settings.
[netlify]
  captcha = true  # Enable CAPTCHA challenge to reduce spam?
+++


<div class="mb-3"><form name="contact" method="post" action="https://formspree.io/bengukalo@gmail.com"><div class="form-group form-inline"><label class="sr-only" for="inputName">Name</label>
<input type="text" name="name" class="form-control w-100" id="inputName" placeholder="Name" required=""></div><div class="form-group form-inline"><label class="sr-only" for="inputEmail">Email</label>
<input type="email" name="email" class="form-control w-100" id="inputEmail" placeholder="Email" required=""></div><div class="form-group"><label class="sr-only" for="inputMessage">Message</label>
<textarea name="message" class="form-control" id="inputMessage" rows="5" placeholder="Message" required=""></textarea></div><button type="submit" class="btn btn-outline-primary px-3 py-2">Send</button></form></div>