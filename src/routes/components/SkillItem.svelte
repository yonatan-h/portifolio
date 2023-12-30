<script>
    export let title = 'title';
    export let imageSrc = '';
</script>

<li class="flex gap-3">
    <img class="w-[1.5rem] h-[1.5rem]" src={imageSrc} alt={title}>
    <span>{title}</span>
</li>