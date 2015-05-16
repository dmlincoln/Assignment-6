Loop.php


<?php
/*
Template Name: Portfolio
*/
>?

<?php get_header();  ?>

<div id="content">

<?php

<!-- Start Loop -->
$loop = new WP_Query(array
    ('post-type' => 'portfolio',
    'posts_per_page' =>10));
?>

<?php while ( $loop->have_posts()
) : $loop->the_post(); ?>

<div class="portfolio-listing">
<h2> <a href="<?php
    the_permalink(); ?>"><?php
    the_title90; ?></a></h2>
    
<?php the_post_thumbnail(
    'portolio-thumb' );?>
    
<php the_content();?>
</div>

<!--End Loop-->

<!-- To Call Footer-->
<?php endwhile; ?>
</div>
<?php get_footer(): ?>

<!--End Footer -->
    
