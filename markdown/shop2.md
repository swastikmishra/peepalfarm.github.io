<!--
Title: Contact us
Scripts: 
- https://www.e-junkie.com/e-junkie-shop-script.js
Javascript: var ej = new EJ_Shop({client_id:328984, pinned:['pntbtr', '1556556', '1564515']});
-->

<div class="container">
	<input class="input" type="text" placeholder="Search Products" id="ej_search_handler">
	<select id="ej_sort_handler">
		<option value="Latest">Latest</option>
		<option value="Popular">Popular</option>
	</select>
	<div id="app_container"></div>
</div>
<div id="listing_template" hidden>
	<div class="row" id="{identifier}" style="{style}">
	 	<div class="one-full column">
    		{form}
    		<div style="float: left; max-width: 40%;"> 
    			<p><strong><a>{title}</a></strong><br/>{tagline}</p>
    			<img src="{thumbnail}" alt="{title}" title="{title}" style="max-width: 200px">
    		</div>
    		<div style="float: right; max-width: 60%;"> 
				<quote>{description}</quote>
				<p>{details}</p>
				{options_template}
    			<p>₹{price}</p>
    			<a href="{link}" target="{link_target}" class="{link_class}" onclick="{onclick}">Add To Cart</a>
    		</div>    
    		{/form}
  		</div>
	</div>
</div>
<div id="dropdown_template" hidden>
	<label class="label">{label}</label>
	{hidden}
	<select name="{name}" style="max-width: 250px">{options}</select>
</div>
<div id="text_template" hidden>
	<label class="label">{label}</label>
	{hidden}
</div>
