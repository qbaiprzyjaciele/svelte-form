<script>
    export let backCallback;

    let notificationType = '';
    let notificationScheduler = '';
    export let cronSchedulerValue  = '';

</script>


<label for="notificationType">Notification type</label>
<select bind:value={notificationType} id="notificationType">
    <option value="email">Email notification</option>
    <option value="inapp">In-app notification</option>
</select>

<label for="notificationScheduler">Notification scheduler</label>
<select bind:value={notificationScheduler} id="notificationScheduler">
    <option value="everyDay9AM">"Daily at 9:00 AM"</option>
    <option value="cronExpression">Cron expression</option>
</select>



{#if notificationScheduler === 'cronExpression'}
    <label for="cronSchedulerValue">Cron expression</label>
    <input type="text" bind:value={cronSchedulerValue} id="cronSchedulerValue">
{/if}
<p>
    <button on:click={backCallback}>Back</button>
</p>

