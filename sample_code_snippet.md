photo_right shortcode

{{< photo_right photo="img/On Roseberry Topping.jpeg"
  photo_alt="Trig Point"
  photo_caption="Trig Point on Roseberry Topping" >}}

Here's what I used in my original walking posts:
(Must have blank lines before and after.)

<figure style="float: right;margin:5px 5px 8px 5px">
  <img  src="/img/finger_pointer.png" alt="Finger Post" >
  <figcaption>Finger Post Points the Way</figcaption>
</figure> 

<figure style="float: right;margin:5px 5px 8px 5px">
  <img  src="img/On Roseberry Topping.jpeg" 
  alt="Trig Point"  width="288" >
  <figcaption>Trig Point on Roseberry Topping</figcaption>
</figure> 


{{< figure 
  title="Landranger 1:50K Sample "
  src="img/Landranger Ivybridge.jpg#floatleft"  
  width="300" attr="Ordnance Survey Crown Copyright"
  alt="Sample Landranger map for Ivybridge"
  attrlink="https://shop.ordnancesurvey.co.uk/apps/os-maps/"
  caption="<font size=2>Landranger 1:50K </font><br><br>" >}}
{{< figure 
  title="Explorer 1:25K Sample"
  src="img/Explorer Ivybridge.jpg#right"  
  width="300"  attr="Ordnance Survey Crown Copyright"
  attrlink="https://shop.ordnancesurvey.co.uk/apps/os-maps/"
  alt="Sample Explorer map for Ivybridge"
  caption="<font size=2>Explorer 1:25K </font><br><br>" >}}
  
later example, replaced by raw html
{{< figure 
  title="Landranger 1:50K Sample "
  src="img/Landranger Ivybridge.jpg#floatleft"  
  width="300" attr="Ordnance Survey Crown Copyright"
  alt="Sample Landranger map for Ivybridge"
  attrlink="https://shop.ordnancesurvey.co.uk/apps/os-maps/" >}}
{{< figure 
  title="Explorer 1:25K Sample"
  src="img/Explorer Ivybridge.jpg#right"  
  width="300"  attr="Ordnance Survey Crown Copyright"
  attrlink="https://shop.ordnancesurvey.co.uk/apps/os-maps/"
  alt="Sample Explorer map for Ivybridge" >}}
And the above shortcode produced this html:
<p><figure>
    <img src="img/Landranger%20Ivybridge.jpg#floatleft"
         alt="Sample Landranger map for Ivybridge" width="300"/> <figcaption>
            <h4>Landranger 1:50K Sample </h4><p>
                    <a href="https://shop.ordnancesurvey.co.uk/apps/os-maps/">Ordnance Survey Crown Copyright</a></p>
        </figcaption>
</figure>

<figure>
    <img src="img/Explorer%20Ivybridge.jpg#right"
         alt="Sample Explorer map for Ivybridge" width="300"/> <figcaption>
            <h4>Explorer 1:25K Sample</h4><p>
                    <a href="https://shop.ordnancesurvey.co.uk/apps/os-maps/">Ordnance Survey Crown Copyright</a></p>
        </figcaption>
</figure>
  
This is what I ended up using:
<figure>
  <figcaption style="font-size:1.2em">OS Maps Examples at Different Zoom Levels</figcaption>
  <figure>
    <figcaption style="font-size:1.2em">Landranger 1:50K</figcaption> 
    <img src="img/Landranger Ivybridge.jpg#floatleft"
    width="300" attr="Ordnance Survey Crown Copyright"
    alt="Sample Landranger map for Ivybridge"  >
  </figure>
  <figure>
    <figcaption style="font-size:1.2em">Explorer 1:25K</figcaption>
    <img src="img/Explorer Ivybridge.jpg#right"
    width="300" attr="Ordnance Survey Crown Copyright"
    alt="Sample Landranger map for Ivybridge" >
  </figure>
    <figcaption style="color:gray;font-size:0.8em;"><a href="https://shop.ordnancesurvey.co.uk/apps/os-maps/">Ordnance Survey Crown Copyright</a></figcaption>
</figure>
      