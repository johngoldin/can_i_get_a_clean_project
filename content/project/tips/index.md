    #### [Back to UK Walking Topics]({{< relref "2017-03-07-an-american-walking-in-britain.md#topics" >}})

    - [Choosing a path]({{< relref "2017-03-11-american-walker-in-britain-part-2.md#choosing-a-path" >}})

<<<<<<< HEAD
    If your writing documentation for Hugo shortcodes, you will need to 
    escape the shortcode processing. e.g., 

    {{</* code */>}} will be rendered as {{< code >}}.
=======
>>>>>>> master
[Hugo figure shortcode](https://gohugo.io/content-management/shortcodes/#figure)

    and {{%/* figure src="/img/taxi.png#floatright" caption="Need a taxi Hadrians Wall Path?" */%}}
     img style="float: right;" src="/img/taxi.png"> 
    <figure.right  > 
      <img  src="/img/taxi.png" alt="taxi phone number" ">
      <figcaption>Isn't this better than camping?</figcaption>
       
    </figure>

    markdown code for figure: (html parameters within curly braces)
    ![(*Text, italic in ()*)](/img/hugo_pool/page_inspector.jpg){width=100%}

    {{%/* figure src="/img/taxi.png#floatright" caption="Need a taxi Hadrians Wall Path?" */%}}

    Have to use shortcode function to embed shortcode from RMarkdown:
    blogdown::shortcode("figure", src = "/img/taxi.png#floatright", caption = "Called using shortcode function")

{{% figure src="/img/taxi.png#floatright" caption="Called using shortcode function" %}}

[workflow for blogdown and netlify](https://www.garrickadenbuie.com/blog/blogdown-netlify-new-post-workflow/)  