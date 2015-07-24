# CountDown-jQuery-plugin
CountDown-jQuery-plugin

#Ways to set the countdown
####Initiate Countdown
<pre><code>jQuery(document).ready(function() {
	$('#countdown_dashboard').countDown({
		targetOffset: {
			'day': 		0,
			'month': 	0,
			'year': 	0,
			'hour': 	0,
			'min': 		0,
			'sec': 		0
		}
	});
});</code></pre>
####Set by specific date/time
<pre><code>function set_by_date() {
	$('#countdown_dashboard').stopCountDown();
	$('#countdown_dashboard').setCountDown({
		targetDate: {
			'day': 		15,
			'month': 	1,
			'year': 	2011,
			'hour': 	12,
			'min': 		0,
			'sec': 		0
		}
	});
	$('#countdown_dashboard').startCountDown();
}</code></pre>
####Set by date/time offset
<pre><code>function set_by_offset() {
	$('#countdown_dashboard').stopCountDown();
	$('#countdown_dashboard').setCountDown({
		targetOffset: {
			'day': 		1,
			'month': 	1,
			'year': 	0,
			'hour': 	1,
			'min': 		1,
			'sec': 		1
		}
	});
	$('#countdown_dashboard').startCountDown();
}</code></pre>


#Start/Stop/Reset
####Set the Countdown
<pre><code>jQuery(document).ready(function() {
	$('#countdown_dashboard').countDown({
		targetOffset: {
			'day': 		1,
			'month': 	1,
			'year': 	0,
			'hour': 	1,
			'min': 		1,
			'sec': 		1
		}
	});
});</code></pre>
####Stop countdown
<pre><code>function stop() {
	$('#countdown_dashboard').stopCountDown();
}</code></pre>
####Start countdown
<pre><code>function start() {
	$('#countdown_dashboard').startCountDown();
}</code></pre>
####reset and start
<pre><code>function reset() {
	$('#countdown_dashboard').stopCountDown();
	$('#countdown_dashboard').setCountDown({
		targetOffset: {
			'day': 		1,
			'month': 	1,
			'year': 	0,
			'hour': 	1,
			'min': 		1,
			'sec': 		1
		}
	});				
	$('#countdown_dashboard').startCountDown();
}</code></pre>


#onComplete event
<pre><code>// Set the Countdown
jQuery(document).ready(function() {
	$('#countdown_dashboard').countDown({
		targetOffset: {
			'day': 		0,
			'month': 	0,
			'year': 	0,
			'hour': 	0,
			'min': 		0,
			'sec': 		5
		}, 
		// onComplete function
		onComplete: function() { $('#complete_info_message').slideDown() }
	});
});</code></pre>


#Multiple instances
<pre><code>jQuery(document).ready(function() {
	// Set the first Countdown
	$('#countdown_dashboard').countDown({
		targetOffset: {
			'day': 		1,
			'month': 	1,
			'year': 	0,
			'hour': 	1,
			'min': 		1,
			'sec': 		5
		}
	});

	// Set the second Countdown
	$('#countdown_dashboard2').countDown({
		targetOffset: {
			'day': 		10,
			'month': 	1,
			'year': 	0,
			'hour': 	6,
			'min': 		34,
			'sec': 		10
		}
	});
});
</code></pre>


#Omit weeks (3-digit days)
<pre><code>// Initiate Countdown
jQuery(document).ready(function() {
	$('#countdown_dashboard').countDown({
		targetOffset: {
			'day': 		0,
			'month': 	0,
			'year': 	1,
			'hour': 	0,
			'min': 		0,
			'sec': 		3
		},
		omitWeeks: true
	});
});
</code></pre>


#Standard time (UTC)
<pre><code>// Initiate Countdown
jQuery(document).ready(function() {
	$('#countdown_dashboard').countDown({
		targetDate: {
			'day': 		17,
			'month': 	12,
			'year': 	2010,
			'hour': 	01,
			'min': 		0,
			'sec': 		0,
			// time set as UTC 
			'utc':		true
		}
	});
});
</code></pre>
