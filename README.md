# WP REST API - Filter parameter for posts endpoints

__NOTE:__ Modified version that allows the meta fields we use to track page views to be filtered in our Playbook CMS REST API endpoint for pages. 

In WordPress 4.7 the `filter` argument for any post endpoint was removed, The `filter` argument allows the posts to be
filtered using `WP_Query` public query vars. This plugin restores the `filter` parameter for sites that were
previously using it.

## Usage

Use the `filter` parameter on any post endpoint such as `/wp/v2/posts` or `/wp/v2/pages` as an array of `WP_Query`
argument like so:

```javascript
fetch( 'https://example.com/wp-json/wp/v2/posts?filter[name]=the-slug');
```
