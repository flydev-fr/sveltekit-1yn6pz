<script>
import { onMount } from 'svelte'
import DailyIframe from '@daily-co/daily-js'


onMount(async () => {
  let callObject = DailyIframe.createFrame();
  const stream = await navigator.mediaDevices.getUserMedia({ audio: true })
  let recorder = new MediaRecorder(stream)
  recorder.start()
})
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
