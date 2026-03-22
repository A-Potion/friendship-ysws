<script>
    import '../app.css';
    import '$lib/fonts.css'
    let { children } = $props();
</script>

<style>
body {
    font-family: 'Hammersmith One';
}
</style>

{@render children()}