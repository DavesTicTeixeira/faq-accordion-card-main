<script>
  let womanmobile = "/images/illustration-woman-online-mobile.svg";
  let icon = "./images/icon-arrow-down.svg";
  let Q1 = false;
  let Q2 = false;
  let Q3 = false;
  let Q4 = false;
  let Q5 = false;
  const toggleQ1 = () => (Q1 = !Q1);
  const toggleQ2 = () => (Q2 = !Q2);
  const toggleQ3 = () => (Q3 = !Q3);
  const toggleQ4 = () => (Q4 = !Q4);
  const toggleQ5 = () => (Q5 = !Q5);
</script>

<div class="main">
  <div class="head">
    <img
      class="womanmobile"
      src={womanmobile}
      alt="illustration-woman-online-mobile"
    />
  </div>
  <div class="faq">
    <div><h1>FAQ</h1></div>
    <p class="question" on:click={toggleQ1} class:selected={Q1}>
      How many team members can I invite?<span
        ><img src={icon} alt="icon" /></span
      >
    </p>
    {#if Q1}
      <p class="answer">
        You can invite up to 2 additional users on the Free plan.
      </p>
    {/if}
    <hr />
    <p class="question" on:click={toggleQ2} class:selected={Q2}>
      What is the maximum file upload size?<span
        ><img src={icon} alt="icon" /></span
      >
    </p>
    {#if Q2}
      <p class="answer">
        No more than 2GB. All files in your account must fit your allotted
        storage space.
      </p>
    {/if}
    <hr />
    <p class="question" on:click={toggleQ3} class:selected={Q3}>
      There is no limit on team members for the Premium plan. What is the
      maximum file upload size?<span><img src={icon} alt="icon" /></span>
    </p>
    {#if Q3}
      <p class="answer">
        No more than 2GB. All files in your account must fit your allotted
        storage space.
      </p>
    {/if}
    <hr />
    <p class="question" on:click={toggleQ4} class:selected={Q4}>
      How do I reset my password?<span><img src={icon} alt="icon" /></span>
    </p>
    {#if Q4}
      <p class="answer">
        Click “Forgot password” from the login page or “Change password” from
        your profile page. A reset link will be emailed to you.
      </p>
    {/if}
    <hr />
    <p class="question" on:click={toggleQ5} class:selected={Q5}>
      Can I cancel my subscription?<span><img src={icon} alt="icon" /></span>
    </p>
    {#if Q5}
      <p class="answer">
        Yes! Send us a message and we’ll process your request no questions
        asked. Do you provide additional support? Chat and email support is
        available 24/7. Phone lines are open during normal business hours.
      </p>
    {/if}
    <hr />
  </div>
</div>

<style>
  .main {
    box-sizing: border-box;
    height: 99vh;
    margin: 0;
    padding: 0;
    display: flex;
    background-color: hsl(273, 75%, 66%);
    min-width: 375px;
    flex-direction: column;
    justify-content: center;
    padding-bottom: 50px;
    font-family: "Kumbh Sans", sans-serif;
    font-size: 12px;
    color: hsl(240, 6%, 50%);
    overflow: scroll;
    font-weight: 400;
  }

  .womanmobile {
    width: 200px;
    z-index: 999;
    margin-inline: 75px;
  }

  .head {
    padding: 50px;
    z-index: 999;
    background-image: url(./images/bg-pattern-mobile.svg);
  }

  .faq {
    width: max-content;
    background-color: white;
    z-index: 000;
    margin: -115px auto auto auto;
    padding-bottom: 50px;
    border-radius: 15px;
    padding-inline: 10px;
  }

  .faq h1 {
    margin-top: 100px;
    margin-bottom: 50px;
    font-size: 30px;
    text-align: center;
    color: hsl(237, 12%, 33%);
  }

  .question {
    padding-block: 10px;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    max-width: 300px;
  }

  .selected {
    color: hsl(237, 12%, 33%);
    font-weight: bold;
    line-height: 200%;
  }

  .answer {
    max-width: 300px;
    padding-block: 10px;
  }

  hr {
    color: hsl(240, 5%, 91%);
  }
</style>
