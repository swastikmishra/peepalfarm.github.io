<!--
Title: Shop 2 Beta
Scripts: 
- https://www.e-junkie.com/e-junkie-shop-script.js
Javascript: var ej = new EJ_Shop({client_id:328984,offset:8,lazy_loading_eff:400,pinned:['pntbtr', '1556556', '1564515']});
-->
<style>
.input_div{
	margin-top: 10vh;
}
.input_div input{ width: 48%; margin-right: 1%; }
.input_div select{ width: 48%; margin-right: 1%; }
.row{
	margin-bottom: 10px;
}
.my_column { width: 50%; padding: 10px; }
.my_column { width: 50%; padding: 10px; }
.cart_btn{
	text-decoration: none;
	background-color: #009900;
	padding: 10px;
	border-radius: 3px;
	color: #fff;
	margin-top: 15px;
	display: block;
	width: fit-content;
}
.label{
	margin-top: 10px;
}
.input, select{
	margin-bottom: 0px;
}
@media(max-width: 600px){
	.my_column{
		width: 100%;
	}
}
</style>

<div class="input_div" style="margin-top: 10vh">
	<input class="input" type="text" placeholder="Search Products" id="ej_search_handler">
	<select id="ej_sort_handler">
		<option value="Latest">Latest</option>
		<option value="Popular">Popular</option>
	</select>
	<div id="app_container"></div>
</div>
<div id="listing_template" hidden>
	<div class="row" id="{identifier}" style="{style}">
	 		<div class="my_column">
    			<p><strong><a>{title}</a></strong><br/>{tagline}</p>
    			<img src="{thumbnail}" alt="{title}" title="{title}" style="max-width: 200px">
<!-- 			<p style="font-size: 13px;">{details}</p> -->
    		</div>
    		<div class="my_column"> 
<!-- 			<quote style="font-size: 12px;">{description}</quote> -->
			{form}
			{options_template}
    			<p>₹{price}</p>
    			<a href="{link}" target="{link_target}" class="cart_btn {link_class}" onclick="{onclick}">Add To Cart</a>
			{/form}
    		</div>    
	</div>
</div>
<div id="dropdown_template" hidden>
	<label class="label">{label}</label>
	{hidden}
	<select name="{name}">{options}</select>
</div>
<div id="text_template" hidden>
	<label class="label">{label}</label>
	<input class="input" type="text" placeholder="{placeholder}" name="{name}">
	{hidden}
</div>
