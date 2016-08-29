# CSS-Tabs
Pure CSS Tabs

## Getting Started

The tabs are created in CSS only, no JS used. The process is very easy to replicate and adding new tabs is also pretty easy. 

### Example 
```
<input type="radio" id="tab1" name="tabGroup1" class="tab" checked>
<label for="tab1">Section One</label>
```

```
<div class="tab__content">
  <h3>Section One</h3>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
</div>
```
### Demo
[Demo](https://cdn.rawgit.com/ducblog/Collect/master/CSS-tabs/index.html)

<p>Just another animated, fully responsive tabs component implemented in pure CSS / CSS3 that uses radio buttons to switch between tabbed panels by clicking on the tab navigation. You will see a vertical accordion when you open the demo page on small screens.</p>
<h2>How to use it:</h2>
<p>The required html structure for the tabs component.</p>
<pre class="brush:xml">&lt;div class="tab-wrap"&gt;

  &lt;input type="radio" id="tab1" name="tabGroup1" class="tab" checked&gt;
  &lt;label for="tab1"&gt;Section One&lt;/label&gt;

  &lt;input type="radio" id="tab2" name="tabGroup1" class="tab"&gt;
  &lt;label for="tab2"&gt;Section Two&lt;/label&gt;

  &lt;input type="radio" id="tab3" name="tabGroup1" class="tab"&gt;
  &lt;label for="tab3"&gt;Section Three&lt;/label&gt;

  &lt;div class="tab__content"&gt;
    &lt;h3&gt;Section One&lt;/h3&gt;
  &lt;/div&gt;

  &lt;div class="tab__content"&gt;
    &lt;h3&gt;Section Two&lt;/h3&gt;
  &lt;/div&gt;

  &lt;div class="tab__content"&gt;
    &lt;h3&gt;Section Three&lt;/h3&gt;
  &lt;/div&gt;

&lt;/div&gt;</pre>
<p>The primary CSS/CSS3 styles.</p>
<pre class="brush:css">.tab-wrap {
  -webkit-transition: 0.3s box-shadow ease;
  transition: 0.3s box-shadow ease;
  border-radius: 6px;
  max-width: 100%;
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  -webkit-flex-wrap: wrap;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  position: relative;
  list-style: none;
  background-color: #fff;
  margin: 40px 0;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
}

.tab-wrap:hover { box-shadow: 0 12px 23px rgba(0, 0, 0, 0.23), 0 10px 10px rgba(0, 0, 0, 0.19); }

.tab { display: none; }

.tab__content {
  padding: 10px 25px;
  background-color: transparent;
  position: absolute;
  width: 100%;
  z-index: -1;
  opacity: 0;
  left: 0;
  -webkit-transform: translateY(-3px);
  transform: translateY(-3px);
  border-radius: 6px;
}</pre>
<p>The radio button + label hacks.</p>
<pre class="brush:css">.tab:checked:nth-of-type(1) ~ .tab__content:nth-of-type(1) {
  opacity: 1;
  -webkit-transition: 0.5s opacity ease-in, 0.2s transform ease;
  transition: 0.5s opacity ease-in, 0.2s transform ease;
  position: relative;
  top: 0;
  z-index: 100;
  -webkit-transform: translateY(0px);
  transform: translateY(0px);
  text-shadow: 0 0 0;
}

.tab:checked:nth-of-type(2) ~ .tab__content:nth-of-type(2) {
  opacity: 1;
  -webkit-transition: 0.5s opacity ease-in, 0.2s transform ease;
  transition: 0.5s opacity ease-in, 0.2s transform ease;
  position: relative;
  top: 0;
  z-index: 100;
  -webkit-transform: translateY(0px);
  transform: translateY(0px);
  text-shadow: 0 0 0;
}

.tab:checked:nth-of-type(3) ~ .tab__content:nth-of-type(3) {
  opacity: 1;
  -webkit-transition: 0.5s opacity ease-in, 0.2s transform ease;
  transition: 0.5s opacity ease-in, 0.2s transform ease;
  position: relative;
  top: 0;
  z-index: 100;
  -webkit-transform: translateY(0px);
  transform: translateY(0px);
  text-shadow: 0 0 0;
}

.tab:checked:nth-of-type(4) ~ .tab__content:nth-of-type(4) {
  opacity: 1;
  -webkit-transition: 0.5s opacity ease-in, 0.2s transform ease;
  transition: 0.5s opacity ease-in, 0.2s transform ease;
  position: relative;
  top: 0;
  z-index: 100;
  -webkit-transform: translateY(0px);
  transform: translateY(0px);
  text-shadow: 0 0 0;
}

.tab:first-of-type:not(:last-of-type) + label {
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}

.tab:not(:first-of-type):not(:last-of-type) + label { border-radius: 0; }

.tab:last-of-type:not(:first-of-type) + label {
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}

.tab:checked + label {
  background-color: #fff;
  box-shadow: 0 -1px 0 #fff inset;
  cursor: default;
}

.tab:checked + label:hover {
  box-shadow: 0 -1px 0 #fff inset;
  background-color: #fff;
}

.tab + label {
  width: 100%;
  box-shadow: 0 -1px 0 #eee inset;
  border-radius: 6px 6px 0 0;
  cursor: pointer;
  display: block;
  text-decoration: none;
  color: #333;
  -webkit-box-flex: 3;
  -webkit-flex-grow: 3;
  -ms-flex-positive: 3;
  flex-grow: 3;
  text-align: center;
  background-color: #f2f2f2;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  text-align: center;
  -webkit-transition: 0.3s background-color ease, 0.3s box-shadow ease;
  transition: 0.3s background-color ease, 0.3s box-shadow ease;
  height: 50px;
  box-sizing: border-box;
  padding: 15px;
}
@media (min-width:768px) {

.tab + label { width: auto; }
}

.tab + label:hover {
  background-color: #f9f9f9;
  box-shadow: 0 1px 0 #f4f4f4 inset;
}</pre>
