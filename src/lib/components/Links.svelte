<script>
    export let linkText = 'Error';
    export let linkUrl = '#';
</script>

<li class="">
    <p class="hoverable ml-20 px-10">
        <a class="" href={`#${linkUrl}`}>{linkText}</a>
    </p>
</li>

<style>
    li {
        cursor: default;
    }
</style>