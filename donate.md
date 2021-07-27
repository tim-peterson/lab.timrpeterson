---
layout: page
title: Donate to the Peterson lab.
permalink: /donate/
---

<div class="container-fluid">
<div class="row">
<div class="home col-md-12">

<h3> We receive our funding mainly from the National Institutes of Health. We would be grateful for your contributions to further fund our work on aging. </h3>
<ul>
	<li>WashU's <a href="https://research.wustl.edu/offices/research-development/">development office</a> coordinates all funding for the university. Please reach out to them. </li>
	<li>If you wish to give directly to our Division, please see <a href="https://bonehealth.wustl.edu/giving/">this link</a>.</li> 
	<li>Alternatively, click a button to copy our cryptocurrency address.</li>
</ul> 


<!--ETH
0x00a33C8379B03085Ad0c0B4F6FB38C63dEBa8475
BTC
bc1q7v2enqsjm0hzskatpkc8z200pt6eh9pm4uke75
LTC
ltc1ql9mq8ccg3syqge3lv00n85q862zeujy2gg7sw7
DOGE
DAK6vkgRBLGKh8CxsDtcyk7huayn1wLSXN
-->





<script src="https://cdn.jsdelivr.net/npm/clipboard@2.0.8/dist/clipboard.min.js"></script>

<ul style="list-style:none;">
<li style="margin: 10px">BTC 
	<button class="btn btn-lg m-2" data-clipboard-target="#btc-target">
		<span id="btc-target">bc1q7v2enqsjm0hzskatpkc8z200pt6eh9pm4uke75
</span>
	</button>
</li>

<li style="margin: 10px">ETH 
	<button class="btn btn-lg m-2" data-clipboard-target="#eth-target">
		<span id="eth-target">0x00a33C8379B03085Ad0c0B4F6FB38C63dEBa8475</span>
	</button>
</li>

<li style="margin: 10px">LTC 
	<button class="btn btn-lg m-2" data-clipboard-target="#ltc-target">
		<span id="ltc-target">ltc1ql9mq8ccg3syqge3lv00n85q862zeujy2gg7sw7</span>
	</button>
</li>

<li style="margin: 10px">DOGE 
	<button class="btn btn-lg m-2" data-clipboard-target="#doge-target">
		<span id="doge-target">DAK6vkgRBLGKh8CxsDtcyk7huayn1wLSXN</span>
	</button>
</li>

</ul>

</div>
</div>
</div>

<script>
	var clipboard = new ClipboardJS('.btn');

clipboard.on('success', function(e) {
    console.info('Action:', e.action);
    console.info('Text:', e.text);
    console.info('Trigger:', e.trigger);

    e.clearSelection();
});

clipboard.on('error', function(e) {
    console.error('Action:', e.action);
    console.error('Trigger:', e.trigger);
});
</script>