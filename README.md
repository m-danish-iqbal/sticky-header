# Sticky Header
Simple jQuery plugin for making sticky header.
<br>
<a href="http://plugins.imdanishiqbal.com/sticky-header/" target="_blank">Complete Guide and Demo</a>
<br>
<br>
Wordpress Version: <a href="https://wordpress.org/plugins/advanced-sticky-header/" target="_blank">https://wordpress.org/plugins/advanced-sticky-header/</a>
<h2>HTML</h2>
<pre class="line-numbers language-markup"><code>&lt;script type=&quot;text/javascript&quot; src=&quot;js/jquery.min.js&quot;&gt;&lt;/script&gt; 
&lt;script type=&quot;text/javascript&quot; src=&quot;js/sticky-header.js&quot;&gt;&lt;/script&gt;

&lt;header class=&quot;example&quot;&gt; 
  &lt;!--  header stuff ... --&gt; 
&lt;/header&gt;
</code></pre>


<br><br>
<h2>Call the plugin</h2>
<pre class="line-numbers language-js"><code>$(document).ready(function(){
  $('.example').stickMe(); 
})
</code></pre>

<br><br>

<h2>Plugin classes</h2>
<pre class="line-numbers language-markup"><code>&lt;!-- Now plugin adds classes to your header on page load --&gt; 
&lt;header class=&quot;example stick-me not-sticking&quot;&gt; 
  &lt;!--  header stuff ... --&gt; 
&lt;/header&gt;



&lt;!-- Header is sticky --&gt; 
&lt;header class=&quot;example stick-me sticking&quot;&gt; 
  &lt;!--  header stuff ... --&gt; 
&lt;/header&gt;
</code></pre>

<br><br>
<h2>Something about styles</h2>
<pre><code class="language-css">
/* Make sure your header has z-index and background set and it's also full width */
.example {
  width: 100%;
  z-index: 999;
  background-color: #ffffff;
}

/* OR you can also style plugin's class .sticking, 
that way you can style it differently when it's sticking */
.sticking {
  width: 100%;
  z-index: 999;
  background-color: #ffffff;
}</code></pre>
<div id="options"></div>

<br><br>
<h2>Defaults</h2>
 
<pre><code class="language-js">transitionDuration: 300,
shadow: false,
shadowOpacity: 0.3,
animate: true,
triggerAtCenter: true,
transitionStyle: 'fade',
stickyAlready: false</code></pre>
          




<br><br>
  <h2>Customizing</h2>
  <div>
    <div>
      <table class="bordered responsive-table">
        <thead>
          <tr>
              <th data-field="variable" style="min-width: 140px;">Variable</th>
              <th data-field="type" style="min-width: 100px;">Type</th>
              <th data-field="example" style="min-width: 190px;">Example</th>
              <th data-field="description">Description</th>
          </tr>
        </thead>

  <tbody>
    <tr>
      <td>topOffset</td>
      <td>int</td>
      <td><div class="chip">topOffset: 300</div></td>
      <td><span> Header will become sticky when the body is scrolled down by 300 pixels</span></td>
    </tr>
    <tr>
      <td>shadow</td>
      <td>boolean</td>
      <td><div class="chip">shadow: true</div></td>
      <td><span> Header will have shadow when it becomes sticky</span></td>
    </tr>
    <tr>
      <td>shadowOpacity</td>
      <td>float</td>
      <td><div class="chip">shadowOpacity: 0.5</div></td>
      <td><span> This sets the opacity of shadow that header gets when it's sticky</span></td>
    </tr>
    <tr>
      <td>animate</td>
      <td>boolean</td>
      <td><div class="chip">animate: true</div></td>
      <td><span> This brings header into display smoothly</span></td>
    </tr>
    <tr>
      <td>transitionStyle</td>
      <td>string</td>
      <td><div class="chip">transitionStyle: 'fade'</div></td>
      <td><span> Transition style for header when it becomes sticky</span> <div class="chip">'fade'</div> <div class="chip">'slide'</div></td>
    </tr>
    <tr>
      <td>triggetAtCenter</td>
      <td>boolean</td>
      <td><div class="chip">triggerAtCenter: false</div></td>
      <td><span> By default header becomes sticky when it reaches the center of viewport, setting it to false will make header sticky just when header is scrolled out of the viewport</span></td>
    </tr>
    <tr>
      <td>stickyAlready</td>
      <td>boolean</td>
      <td><div class="chip">stickyAlready: true</div></td>
      <td><span> Makes header sticky when page loads</span></td>
    </tr>
    <tr>
      <td>transitionDuration</td>
      <td>int</td>
      <td><div class="chip">transitionDuration: 1000</div></td>
      <td><span> Transition duration of animation</span></td>
    </tr>
  </tbody>
</table>
</div>
  </div>


  <br>
  <br>
  <h2>Events</h2>
  <div class="card-panel">
    <table class="bordered responsive-table">
        <thead>
          <tr>
              <th data-field="variable" style="min-width: 140px;">Event</th>
              <th data-field="description">Description</th>
          </tr>
        </thead>

  <tbody>
    <tr>
      <td>sticky-begin</td>
      <td><span> When header gets sticky</span></td>
    </tr>
    <tr>
      <td>sticking</td>
      <td><span> When header is sticking (This event is called every time page is scrolled and header is sticky)</span></td>
    </tr>
    <tr>
      <td>top-reached</td>
      <td><span> When document's top is reached</span></td>
    </tr>
    <tr>
      <td>bottom-reached</td>
      <td><span> When document's bottom is reached</span></td>
    </tr>
  </tbody>
  </table>
  </div>

  <br><br>
<h2>Using Events</h2>
<pre class="line-numbers language-js"><code>$(document).ready(function(){
  $('.site-header').on('sticky-begin', function() { 
    console.log("Began"); 
  });

  $('.site-header').on('sticking', function() { 
    console.log("Sticking"); 
  });

  $('.site-header').on('top-reached', function() { 
    console.log("Top reached"); 
  });

  $('.site-header').on('bottom-reached', function() { 
    console.log("Bottom reached"); 
  });
})

</code></pre>
