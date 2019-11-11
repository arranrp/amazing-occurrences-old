---
title: Get Yours
layout: layouts/base.njk
subtitle: Clone and deploy your own EleventyOne starter template.
---

## Sign Up

This site is deployed by, and hosted by [Netlify](https://www.netlify.com).

<form name="amazing-occurrences-mailchimp" method="POST" data-netlify="true">
  <p>
    <label>Your Name: <input type="text" name="name" /></label>   
  </p>
  <p>
    <label>Your Email: <input type="email" name="email" /></label>
  </p>
  <p>
    <label>Your Role: <select name="role[]" multiple>
      <option value="leader">Leader</option>
      <option value="follower">Follower</option>
    </select></label>
  </p>
  <p>
    <label>Message: <textarea name="message"></textarea></label>
  </p>
  <p>
    <button type="submit">Send</button>
  </p>
</form>

<script type="text/javascript">
	$("#amazing-occurrences-mailchimp").submit(function(e) {
	  e.preventDefault();

	  var $form = $(this);
	  $.post($form.attr("action"), $form.serialize()).then(function() {
	    alert("Thank you!");
	  });
	});
</script>