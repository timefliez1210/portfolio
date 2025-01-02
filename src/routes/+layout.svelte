<script>
    import Header from '../components/Header.svelte';
    import Navigation from '../components/Navigation.svelte';
    import Background from '../components/Background.svelte';
    import Footer from '../components/Footer.svelte';
</script>
<Background />
<Navigation />
<Header />
<slot></slot>
<Footer />