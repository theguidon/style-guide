# PHP and WordPress Template Style Guide

## Inserting HTML in PHP
- When adding HTML elements in your PHP Template, _DO NOT_ `echo` the HTML out.
Instead, close your PHP then add your HTML
~~~~~~PHP
<!-- Wrong -->
<?php
  if(have_posts()): while(have_posts()): the_post();
  echo '<div>';
  the_content();
  echo '</div>';
?>

<!-- Correct -->
<?php if(have_posts()): while(have_posts()): the_post(); ?>
<div>
  <?php the_content(); ?>
</div>
<?php endwhile; endif;>
~~~~~~

## Indentations
- Always use 2 spaces

## Control Structures
- Common control structures within WP Templates include the `if` and `while`.
When using these, always use the colon syntax.
~~~~~~PHP
<?php if(have_posts()): while(have_posts()): the_post(); ?>
  // Do Something Here
<?php endwhile; endif;>
~~~~~~
