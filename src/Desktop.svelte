<script>
  let womanmobile = "/images/illustration-woman-online-mobile.svg";
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

<body>
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
        How many team members can I invite? >
      </p>
      {#if Q1}
        <p class="answer">
          You can invite up to 2 additional users on the Free plan.
        </p>
      {/if}
      <p class="question" on:click={toggleQ2} class:selected={Q2}>
        What is the maximum file upload size? >
      </p>
      {#if Q2}
        <p class="answer">
          No more than 2GB. All files in your account must fit your allotted
          storage space.
        </p>
      {/if}
      <p class="question" on:click={toggleQ3} class:selected={Q3}>
        There is no limit on team members for the Premium plan. What is the
        maximum file upload size? >
      </p>
      {#if Q3}
        <p class="answer">
          No more than 2GB. All files in your account must fit your allotted
          storage space.
        </p>
      {/if}
      <p class="question" on:click={toggleQ4} class:selected={Q4}>
        How do I reset my password? >
      </p>
      {#if Q4}
        <p class="answer">
          Click “Forgot password” from the login page or “Change password” from
          your profile page. A reset link will be emailed to you.
        </p>
      {/if}
      <p class="question" on:click={toggleQ5} class:selected={Q5}>
        Can I cancel my subscription? >
      </p>
      {#if Q5}
        <p class="answer">
          Yes! Send us a message and we’ll process your request no questions
          asked. Do you provide additional support? Chat and email support is
          available 24/7. Phone lines are open during normal business hours.
        </p>
      {/if}
    </div>
  </div>
</body>

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
  }

  .womanmobile {
    width: 200px;
    z-index: 999;
    margin-inline: 75px;
  }

  .head {
    padding: 50px;
    z-index: 999;
  }

  .faq {
    width: max-content;
    background-color: white;
    z-index: 000;
    margin: -115px auto auto auto;
    margin-inline: 50px;
    padding-bottom: 50px;
    border-radius: 15px;
  }

  .faq h1 {
    margin-top: 100px;
    font-size: 60px;
    text-align: center;
    color: hsl(237, 12%, 33%);
  }

  .question {
    max-width: 300px;
    padding-inline: 30px;
    cursor: pointer;
  }

  .selected {
    color: hsl(237, 12%, 33%);
    font-weight: bold;
  }

  .answer {
    max-width: 300px;
    padding-inline: 30px;
  }
</style>
