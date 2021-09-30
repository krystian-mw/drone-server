<script lang="ts">
  import Left from './components/Left.svelte'
  import './styles.scss'

  export let name: string

  const data = {
    left: {
      x: 0.5,
      y: 0
    },
    right: {
      x: 0.5,
      y: 0.5
    }
  }
</script>

<div class="container">
  <div class="controllers">
    <div>
      <Left bind:x={data.left.x} bind:y={data.left.y} />
    </div>
    <div>
      <!-- Right -->
    </div>
  </div>
</div>

<style lang="scss">
  .container {
    .controllers {
      width: 100vw;
      display: flex;

      > div {
        flex: 1;
      }
    }
  }
</style>