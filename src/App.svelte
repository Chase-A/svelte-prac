<script>
  import logo from "./assets/svelte.png";
  import Counter from "./components/Counter.svelte";
  import Spacer from './components/Spacer.svelte';
  import DropContainerFlex from "./components/dropdowns/DropContainerFlex.svelte";
  import DropContainerFlexInGrid from "./components/dropdowns/DropContainerFlexInGrid.svelte";
  import DropContainerGrid from "./components/dropdowns/DropContainerGrid.svelte";
  import SortContainer from "./components/sorting/SortContainer.svelte";
  import TimerContainer from "./components/timers/TimerContainer.svelte";
</script>

<main>
  <Spacer />

  <TimerContainer />
  <Spacer />

  <SortContainer />
  <Spacer />

  <DropContainerFlexInGrid />
  <Spacer />

  <DropContainerFlex/>
  <Spacer />

  <DropContainerGrid />
  <Spacer />

  <img src={logo} alt="Svelte Logo" />
  <h1>Hello world!</h1>

  <Counter />

</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  main {
    text-align: center;
  }

  img {
    height: 4rem;
    width: 4rem;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }
</style>
