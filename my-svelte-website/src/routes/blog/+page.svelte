<script lang="ts">
    import BlogCard from "$lib/components/BlogCard.svelte";
    export let data: { posts: Post[] };
    console.log(`Receiving ${data.posts.length} posts.`);
</script>

<section class="mb-16">
    <ul class="flex flex-col items-center">
        {#each data.posts as post}
            <BlogCard {post} />
        {/each}
    </ul>
</section>