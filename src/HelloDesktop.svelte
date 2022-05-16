<script>
  let womandesktop = "/images/illustration-woman-online-desktop.svg";
  let box = "./images/illustration-box-desktop.svg";
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

<body>
  <div class="main">
    <div class="head">
      <img class="boxdesktop" src={box} alt="illustration-box-desktop" />
      <img
        class="womandesktop"
        src={womandesktop}
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
</body>

<style>
  body {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    min-height: 100vh;
    background-color: hsl(273, 75%, 66%);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: "Kumbh Sans", sans-serif;
    font-size: 12px;
    color: hsl(240, 6%, 50%);
  }

  .main {
    background-color: aliceblue;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 100px;
    padding: 50px;
    position: relative;
    min-height: 300px;
    border-radius: 15px;
  }

  .head {
    position: absolute;
    margin-left: -500px;
  }

  .womandesktop {
    background-image: url(./images/bg-pattern-mobile.svg);
    max-width: 350px;
  }

  .boxdesktop {
    position: absolute;
    margin-top: 100px;
    margin-left: -50px;
  }

  .faq {
    margin-left: 300px;
    max-width: 350px;
  }

  h1 {
    font-size: 24px;
    color: hsl(238, 29%, 16%);
    padding-bottom: 50px;
  }

  .question {
    padding-block: 10px;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
  }

  .answer {
    padding-block: 10px;
  }

  hr {
    color: hsl(240, 5%, 91%);
  }

  .selected {
    color: hsl(237, 12%, 33%);
    font-weight: bold;
  }
</style>
