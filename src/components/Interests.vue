<script setup lang="ts">

</script>

<template>
  <section id="interests">
    <h1>Interests</h1>
    <p>I am into quite technical things, although I am definitely an amateur. Here are a list of my fascinations:</p>
    <div class="interest" id="nfa">Even interested in programming language design (NFA/DFA. 3-address code etc)</div>
    <div class="interest" id="coding-theory">Coding Theory</div>
    <div class="interest" id="lisp">Lisp</div>
    <div class="interest" id="combinator-theory">Combinator Theory</div>
    <div class="interest" id="emacs">Emacs (I like the philosophy of Vim too)</div>
    <div class="interest" id="lambda-calculus">Lambda Calculus</div>
    <div class="interest" id="fp">Functional Programming</div>
    <div class="interest" id="regex">Regex (yes, I am one of those people!)</div>
    <div class="interest" id="html-css">HTML+CSS</div>
  </section>
</template>

<style scoped>
  h1 {
    color: #7ED8FF;
  }
  p {
    color: #fff;
  }
  #interests {
    background: var(--primary-color);
    background-image: url("../assets/4pointstar.png");
  }
  .interest {
    background: var(--primary-color);
    position: relative;
    width: fit-content;
    color: #7ED8FF;
    font-size: 1.1rem;
    border: solid 1px #6C4CDF;
    border-radius: 2px;
    padding: 0.75rem;
  }
  #nfa {
    top: 0;
  }
  #coding-theory {
    top: -5px;
    left: calc(30vw);
  }
  #lisp {
    top: -15px;
    left: calc(20vw);
  }
  #combinator-theory {
    top: -20px;
    left: calc(25vw);
  }
  #emacs {
    top: -15px;
    left: calc(5vw);
  }
  #lambda-calculus {
    top: -20px;
    left: calc(25vw);
  }
  #fp {
    top: -15px;
    left: calc(15vw);
  }
  #regex {
    top: -20px;
    left: -15vw;
  }
  #html-css {
    top: -49px;
    left: calc(37vw);
  }
</style>