<script>
let name = 'svelte';
let src = 'https://picsum.photos/200/300';
let string = 'Some <strong>HTML</strong> string';
</script>

<img {src} alt="">
<h1>Hello {name.toUpperCase()}</h1>
<p>{@html string}</p>
<style>
h1 {
  color: red;
}
</style>