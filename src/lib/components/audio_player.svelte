<script context="module">
    const players = new Set()
  
    export function stopAll() {
      players.forEach(p => p.pause())
    }
  </script>
  
  <script>
    import { onMount } from 'svelte'
  
    export let src
    
    let player
  
    onMount(() => {
      // Like players.push(player)
      players.add(player)
    })
  </script>
  
  <div class="audio">
      <audio
          bind:this={player}
          {src}
          controls>
          <track kind="captions" />
      </audio>
  </div>


  <style>
    .audio {
      width: 100%;
      height: 100%;
      position: relative;
      overflow: hidden;
      padding: 20px 0px;
    }

  </style>