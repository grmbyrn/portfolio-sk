<script lang="ts">
	import Project from "$lib/components/portfolio/Project.svelte";
</script>
<Project
    heroMobile={'images/detail/mobile/image-bookmark-hero.jpg'}
    heroTablet={'images/detail/tablet/image-bookmark-hero.jpg'}
    heroDesktop={'images/detail/desktop/image-bookmark-hero.jpg'}
    title={'Torrust'}
    desc={'This project required me to maintain and update a blog in SvelteKit which informs the user on how to use Torrust, an open source project that aims to provide you with the tools you need to host your own torrent indexes with ease.'}
    tags={['SvelteKit', 'HTML', 'Sass', 'TypeScript', 'Markdown']}
    link={'https://torrust.com/'}
    background={"For this project, I worked on an existing SvelteKit blog template which the company had previously adapted for their own blog. As time went on, they wanted to optimise the blog. As the only developer with experience in SvelteKit, it was my responsibility to work with the ideas of colleagues on the team, as well as to contribute my own, and then execute them in the project. Working on this project has helped me work with an existing SvelteKit codebase and collaborate with colleagues on how to make it better suit our needs. The biggest challenge was working with the blog posts as they are all written in Markdown. I was also able to become more comfortable with using TypeScript as part of a SvelteKit project."}
    staticPreviewMobile1={'images/detail/mobile/image-bookmark-preview-1.jpg'}
    staticPreviewTablet1={'images/detail/tablet/image-bookmark-preview-1.jpg'}
    staticPreviewDesktop1={'images/detail/desktop/image-bookmark-preview-1.jpg'}
    staticPreviewMobile2={'images/detail/mobile/image-bookmark-preview-2.jpg'}
    staticPreviewTablet2={'images/detail/tablet/image-bookmark-preview-2.jpg'}
    staticPreviewDesktop2={'images/detail/desktop/image-bookmark-preview-2.jpg'}
    previousProject={'/manage'}
    nextProject={'/insure'}
/>