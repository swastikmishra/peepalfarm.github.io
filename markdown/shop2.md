<!--
Title: Shop 2 Beta
Scripts: 
- https://www.e-junkie.com/e-junkie-shop-script.js
Javascript: var ej = new EJ_Shop({client_id:328984,offset:8,lazy_loading_eff:400,pinned:['pntbtr', '1556556', '1564515']});
-->
<div style="margin-top: 10vh">
	<input class="input" type="text" placeholder="Search Products" id="ej_search_handler">
	<select id="ej_sort_handler">
		<option value="Latest">Latest</option>
		<option value="Popular">Popular</option>
	</select>
	<div id="app_container"></div>
</div>
<div id="listing_template" hidden>
	<div class="row" id="{identifier}" style="{style}">
    		{form}
	 	<div class="one-half column" style="width: 50%;margin-left: 0px;padding-right: 20px;">
    			<p><strong><a>{title}</a></strong><br/>{tagline}</p>
    			<img src="{thumbnail}" alt="{title}" title="{title}" style="max-width: 200px">
			<p style="font-size: 13px;">{details}</p>
    		</div>
    		<div class="one-half column" style="width: 50%;margin-left: 0px; padding-right: 20px; padding-top: 15px; padding-bottom: 20px;"> 
			<quote style="font-size: 12px;">{description}</quote>
			{options_template}
    			<p>₹{price}</p>
    			<a href="{link}" style="text-decoration: none;background-color: #009900;padding: 10px;border-radius: 3px;color: #fff;margin-top: 15px;display: block;width: fit-content;" target="{link_target}" class="{link_class}" onclick="{onclick}">Add To Cart</a>
    		</div>    
    		{/form}
	</div>
</div>
<div id="dropdown_template" hidden>
	<label class="label" style="margin-top: 15px;">{label}</label>
	{hidden}
	<select name="{name}" style="max-width: 250px;margin-bottom: 0px;">{options}</select>
</div>
<div id="text_template" hidden>
	<label class="label" style="margin-top: 15px;">{label}</label>
	<input class="input" type="text" placeholder="{placeholder}" name="{name}" style="margin-bottom: 0px;">
	{hidden}
</div>
