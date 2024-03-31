<script lang="ts">
	import ProjectCard from "$lib/components/portfolio/ProjectCard.svelte";
</script>

<div class="container">
    <ProjectCard
        index={1}
        bgImageMobile={'/images/portfolio/mobile/image-portfolio-manage.jpg'}
        bgImageTablet={'/images/portfolio/tablet/image-portfolio-manage.jpg'}
        bgImageDesktop={'/images/portfolio/desktop/image-portfolio-manage.jpg'}
        title={'Manage'}
        description={'This project required me to build a fully responsive landing page to the designs provided. I used HTML5, along with CSS Grid and JavaScript for the areas that required interactivity, such as the testimonial slider.'}
        link={'/manage'}
    />
    
    <ProjectCard
        index={2}
        bgImageMobile={'/images/portfolio/mobile/image-portfolio-bookmark.jpg'}
        bgImageTablet={'/images/portfolio/tablet/image-portfolio-bookmark.jpg'}
        bgImageDesktop={'/images/portfolio/desktop/image-portfolio-bookmark.jpg'}
        title={'Bookmark'}
        description={'This project required me to build a fully responsive landing page to the designs provided. I used HTML5, along with CSS Grid and JavaScript for the areas that required interactivity, such as the features section.'}
        link={'/bookmark'}
    />
    
    <ProjectCard
        index={3}
        bgImageMobile={'/images/portfolio/mobile/image-portfolio-insure.jpg'}
        bgImageTablet={'/images/portfolio/tablet/image-portfolio-insure.jpg'}
        bgImageDesktop={'/images/portfolio/desktop/image-portfolio-insure.jpg'}
        title={'Insure'}
        description={'This was a small project which mostly consisted of HTML and CSS. I built a fully-responsive landing page. The only JavaScript this project required was to enable the toggling of the mobile navigation.'}
        link={'/insure'}
    />
    
    <ProjectCard
        index={4}
        bgImageMobile={'/images/portfolio/mobile/image-portfolio-fylo.jpg'}
        bgImageTablet={'/images/portfolio/tablet/image-portfolio-fylo.jpg'}
        bgImageDesktop={'/images/portfolio/desktop/image-portfolio-fylo.jpg'}
        title={'Fylo'}
        description={'This project was built in pure HTML and CSS. I had mobile and desktop designs to work to and built it so that it was fully-responsive. I took a mobile-first approach and used modern CSS like Flexbox and Grid for layout purposes.'}
        link={'/fylo'}
    />
</div>

<style>
    .container{
        padding-inline: 2rem;
        margin-top: 2.5rem;
    }
</style>