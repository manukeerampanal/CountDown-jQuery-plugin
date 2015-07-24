# CountDown-jQuery-plugin
CountDown-jQuery-plugin

#Ways to set the countdown
####Initiate Countdown
<code><pre>jQuery(document).ready(function() {
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
});</pre></code>
####Set by specific date/time
<code><pre>function set_by_date() {
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
}</pre></code>
####Set by date/time offset
<code><pre>function set_by_offset() {
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
}</pre></code>


#Start/Stop/Reset
####Set the Countdown
<code><pre>jQuery(document).ready(function() {
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
});</pre></code>
####Stop countdown
<code><pre>function stop() {
	$('#countdown_dashboard').stopCountDown();
}</pre></code>
####Start countdown
<code><pre>function start() {
	$('#countdown_dashboard').startCountDown();
}</pre></code>
####reset and start
<code><pre>function reset() {
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
}</pre></code>


#onComplete event
<code><pre>// Set the Countdown
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
});</pre></code>


#Multiple instances
<code><pre>jQuery(document).ready(function() {
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
</pre></code>


#Omit weeks (3-digit days)
<code><pre>// Initiate Countdown
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
</pre></code>


#Standard time (UTC)
<code><pre>// Initiate Countdown
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
</pre></code>
