<script lang="ts">
</script>

<div>
  <form
    class="flex flex-col justify-center w-min mx-auto"
    action="mailto:recipient@example.com"
    method="get"
    enctype="text/plain"
  >
    <label for="email">Enter your email:</label><br />
    <input
      class="rounded p-2 my-1"
      type="email"
      id="email"
      name="email"
      placeholder="example@gmail.com"
    /><br />
    <label for="query">Enter your message:</label><br />
    <textarea
      class="rounded p-2 my-1"
      name="body"
      rows="5"
      cols="30"
      placeholder="Your Message"
    /><br />
    <input
      class="bg-indigo-200 rounded hover:bg-indigo-400"
      type="submit"
      value="Send"
    />
  </form>
</div>

<style>
</style>
