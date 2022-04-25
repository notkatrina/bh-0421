---
layout: layouts/post.njk
title: About Me
templateClass: tmpl-post
eleventyNavigation:
  key: About Me
  order: 3
---

I am a colormatching tool. Talk to me below! 


<form name="contact" method="POST" data-netlify="true">
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
