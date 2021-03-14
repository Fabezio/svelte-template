<script>
    import {onMount} from 'svelte'
    const timeOptions = {
		hour: "2-digit",
		minute: "2-digit",
		// second: "2-digit"
	}
	
	let date;
	const formatter = Intl.DateTimeFormat('fr', timeOptions);
	onMount(() => {
    const interval = setInterval(() => {
      date = new Date()
    }, 1000);
    // console.log(hours);
    //  if (hours.length < 2) hours = "0" + hours;
    //  if (minutes.length < 2) minutes = "0" + minutes;
    //  if (seconds.length < 2) seconds = "0" + seconds;
    
    return () => {
      clearInterval(interval);
    };
  });

</script>

<div style="self-align: center; padding: 1em" >
    {formatter.format(date)}
    
</div>