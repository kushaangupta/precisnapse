---
layout: page
title: About
permalink: /about/
---

## [The four-question summary](https://github.com/alicelucas/papers)

After I read a paper, I like to write down the answer to four questions:

- ***Why is this work imporant?***
    - This gives me a sense of the application of the paper & why it is
    important. It helps me put things into context & understand the rest of the
    content of the paper better. 
- ***Why is this work different?***
    - The answer to this question tells me what is new or different about the
    method proposed by the authors, when comparing against the rest of the
    current literature. 
- ***How does it work?***
    - This answer delves into some of the technical details of the paper,
    although it still tries to avoid the nitty-gritty and still gives the big
    picture idea. 
- ***What are the results?***
    - This provides any interesting or significant results that are particularly
    important. Any additional comments or thoughts I have would be written as
    well.

---

<div class="container"></div>

<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js" type="text/javascript"></script>
<script src="https://unpkg.com/showdown/dist/showdown.min.js" type="text/javascript"></script>

<script>
$(document).ready(function(){
  $.ajax({
    type: 'GET',
    url: 'https://raw.githubusercontent.com/kushaangupta/kushaangupta/master/README.md',
    dataType: 'text',
    success: function(data) {
      let converter = new showdown.Converter();
      let text = converter.makeHtml(data);
      $(".container").html(text)
    }
  });
});
</script>
