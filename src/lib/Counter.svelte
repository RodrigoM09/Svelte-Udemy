<script>
   let counter1 = 0;
   let counter2 = 0;
    let string;
   // Reactive statements will be executed either when the component is initialized
   // or when the value of the variable changes, in this case, when the counter changes(when the button is clicked)
    $: {
      console.log(`counter changed ${counter1}`);
    }

    $: string = `The count total is ${counter1 + counter2}`;

    function getTotal(counter1, counter2) {
      return counter1 + counter2;
    }

    $: string2 = `The count total is ${getTotal(counter1, counter2)}`;

    function increment() {
      counter1 += 1;
    }
    function increment2() {
      counter2 += 1;
    }
    function decrement() {
      counter1 -= 1;
    }
    function decrement2() {
      counter2 -= 1;
    }
</script>
<div>
    <p>{counter1}</p>
    <h3>{string}</h3>
    <h3>{string2}</h3>
    <button on:click={increment}>Up</button>
    <button on:click={decrement}>Down</button>
    <p>{counter2}</p>
    <button on:click={increment2}>Up2</button>
    <button on:click={decrement2}>Down2</button>
 </div>

 <style>
    div{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 10rem;
        width: 10rem;
    }
    p{
        background-color: beige;
        padding: 1rem;
    }
 </style>