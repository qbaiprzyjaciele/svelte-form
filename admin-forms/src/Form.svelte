<script>
    import BasicInfo from "./BasicInfo.svelte";
    import Contact from "./Contact.svelte";
    import AdditionalInfo from "./AdditionalInfo.svelte";

    export let currentStep = 0;

    export const stepNames = [
        'BASIC_INFO',
        'CONTACT',
        'ADDITIONAL_INFO',
    ];

    const MAX_STEP = 2;
    const MIN_STEP = 0;

    const goToNextStep = () => {
        if(currentStep < MAX_STEP) {
            currentStep += 1;
        }
    };

    const goToPrevStep = () => {
        if(currentStep > MIN_STEP) {
            currentStep -= 1;
        };
    };

</script>

<style>

</style>

<div>
    {#if stepNames[currentStep] === 'BASIC_INFO'}
        <BasicInfo continueCallback={goToNextStep} backCallback={goToPrevStep} />
    {:else if stepNames[currentStep] === 'CONTACT'}
        <Contact continueCallback={goToNextStep} backCallback={goToPrevStep} />
    {:else if stepNames[currentStep] === 'ADDITIONAL_INFO'}
        <AdditionalInfo backCallback={goToPrevStep} />
    {/if}
</div>