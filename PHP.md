# PHP and WordPress Template Style Guide
*Note: Part of this is taken from the [Wordpress Style Guide](https://make.wordpress.org/core/handbook/best-practices/coding-standards/php/)*

- Remove trailing whitespace in your code

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

## Naming Conventions

- Use snake case
~~~~~~PHP
// Wrong
$fooBar
$foo-bar

// Correct
$foo_bar
~~~~~~

## Spacing and Indentations
- Always use 2 spaces
- Always add a space before opening braces

## Associative Arrays
- When you have an associative array, put each key/value pair on one line
- Indent key/value pair in associative arrays
- Align all fat arrows

~~~~~~PHP
$foo = array(
  'key1'          => 'value1',
  'key2'          => 'value2',
  'long_key_name' => 'value3'
);
~~~~~~

## Control Structures
- Common control structures within WP Templates include the `if` and `while`.
If your code has HTML in it, use the colon. Otherwise, the braces are permissible.
~~~~~~PHP
<?php if(have_posts()): while(have_posts()): the_post(); ?>
  <div>
    <?php the_content(); ?>
  </div>
<?php endwhile; endif;>
~~~~~~
