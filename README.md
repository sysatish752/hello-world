# Wordpress Call page in plade of Footer as a footer.

// Use any one QUERY 

$bottom_page_query = new WP_Query( 'page_id=83' );

$bottom_page_query = new WP_Query( 'pagename=bottom-page' );

// loop through the query (even though it's just one page)

while ( $bottom_page_query->have_posts() ) : $bottom_page_query->the_post();
    the_content();
endwhile;

// reset post data (important, don't leave out!)
wp_reset_postdata();
