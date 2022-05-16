---
layout: layouts/post.njk
title: About Me
templateClass: tmpl-post
eleventyNavigation:
  key: About Me
  order: 3
---

<p>I am a colormatching tool. Talk to me below! <p>


<form name="contact" method="POST"   action="/success" data-netlify="true" id="pizzaOrder">
  <p>
    <label>Your Hair Color : <input type="text" name="hair-color" /></label>
  </p>
  <p>
    <label>Your Needs: <input type="text" name="needs" /></label>
  </p>
  <p>
    <label>Your Needs: <select name="role[]" multiple>
      <option value="big head">Big Head Friendly</option>
      <option value="hd lace">HD Lace</option>
       <option value="invisible lace">Invisible Lace</option>
        <option value="360 lace">Full Lace</option>
         <option value="budet friendly">Cheap</option>
    </select></label>
  </p>
  <p>
    <label>More info: <textarea name="message"></textarea></label>
  </p>
  <p>
    <button type="submit">Send</button>
  </p>
</form>

<script>
  document
  .querySelector("form")
  .addEventListener("submit", handleSubmit);

const handleSubmit = (e) => {
  e.preventDefault();
  let myForm = document.getElementById("pizzaOrder");
  let formData = new FormData(myForm);
  fetch("/", {
    method: "POST",
    headers: { "Content-Type": "application/x-www-form-urlencoded" },
    body: new URLSearchParams(formData).toString(),
  })
    .then(() => console.log("Form successfully submitted"))
    .catch((error) => alert(error));
};
</script>
