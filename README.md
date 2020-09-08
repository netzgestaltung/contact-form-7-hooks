# Contact Form 7 Hooks

Here you can find some [Contact Form 7](https://wordpress.org/plugins/contact-form-7/) actions and filters (hooks) available for use. The last used version is 4.2.1.
## Actions in /contact-form-7/includes/contact-form.php 

- `wpcf7_contact_form`

```php
/**
 * Fires after the $cf7 constructor was called
 *
 * @param $cf7  class object
 */
function action_wpcf7_contact_form( $cf7 ) {     
  // do some action
};
add_action( 'wpcf7_contact_form', 'action_wpcf7_contact_form'); 
```


- `wpcf7_submit`

```php
/**
 * Fires after a form has been submitted
 *
 * @param $cf7  class object
 * @param $result  named array 'contact_form_id', 'status', 'message', 'demo_mode'
 */
function action_wpcf7_submit( $cf7, $result ) {     
  // do some action
};
add_action( 'wpcf7_submit', 'action_wpcf7_submit', 10, 2 ); 
```

- `wpcf7_after_create`

```php
/**
 * Fires after a $cf7 form was created
 *
 * @param $cf7  class object
 */
function action_wpcf7_after_create( $cf7 ) {     
  // do some action
};
add_action( 'wpcf7_after_create', 'action_wpcf7_after_create'); 
```

- `wpcf7_after_update`

```php
/**
 * Fires after a $cf7 form was updated
 *
 * @param $cf7  class object
 */
function action_wpcf7_after_update( $cf7 ) {     
  // do some action
};
add_action( 'wpcf7_after_update', 'action_wpcf7_after_update'); 
```


- `wpcf7_after_save`

```php
/**
 * Fires after a $cf7 form was saved
 *
 * @param $cf7  class object
 */
function action_wpcf7_after_save( $cf7 ) {     
  // do some action
};
add_action( 'wpcf7_after_save', 'action_wpcf7_after_save'); 
```


## Filters in /contact-form-7/includes/contact-form.php 

- `wpcf7_contact_form_default_pack`

```php
/**
 * Description
 *
 * @param $contact_form
 * @param $args
 * @return $contact_form
 */
add_filter('wpcf7_contact_form_default_pack', function($contact_form, $args) {
    return $contact_form;
});
```

- `wpcf7_contact_form_properties`

```php
/**
 * Description
 *
 * @param $properties
 * @param $cf7
 * @return $properties
 */
add_filter('wpcf7_contact_form_properties', function($properties, $cf7) {
    return $properties;
});
```

- `wpcf7_subscribers_only_notice`

```php
/**
 * Used to change the form subscribers only notice
 *
 * @param $notice subscribers only notice
 * @return string The new notice you want
 */
add_filter('wpcf7_subscribers_only_notice', function($notice, $cf7) {
    return $notice;
});
```

- `wpcf7_form_action_url`

```php
/**
 * Used to change the form action URL
 *
 * @param $url the current URL
 * @return string The new URL you want
 */
add_filter('wpcf7_form_action_url', function($url) {
    return $url;
});
```

- `wpcf7_form_id_attr`

```php
/**
 * Change de form HTML id value
 *
 * @param $html_id The current id value
 * @return string The new id
 */
add_filter('wpcf7_form_id_attr', function($html_id) {
    return $html_id;
});
```

- `wpcf7_form_name_attr`

```php
/**
 * Change de form HTML name
 *
 * @param $html_name The actual name
 * @return string The new name
 */
add_filter('wpcf7_form_name_attr', function($html_name) {
    return $html_name;
});
```

- `wpcf7_form_class_attr`

```php
/**
 * Change de form class name
 *
 * @param $html_class The actual class name
 * @return string The new class name
 */
add_filter('wpcf7_form_class_attr', function($html_class) {
    return $html_class;
});
```

- `wpcf7_form_enctype`

```php
/**
 * Change de form enctype tag
 *
 * @param $html_enctype An empty string
 * @return string The new enctype tag value
 */
add_filter('wpcf7_form_enctype', function($html_enctype = '') {
    return $html_enctype;
});
```


- `wpcf7_form_autocomplete`

```php
/**
 * Change de form autocomplete attribute
 *
 * @param $autocomplete An empty string
 * @return string The new autocomplete attribute "autocomplete"
 */
add_filter('wpcf7_form_autocomplete', function($autocomplete = '') {
    return $autocomplete;
});
```

- `wpcf7_form_novalidate`

```php
/**
 * Description
 *
 * @param $support_html5 The result of wpcf7_support_html5() function call
 * @return @novalidate
 */
add_filter('wpcf7_form_novalidate', function($support_html5) {
    return null;
});
```

- `wpcf7_form_hidden_fields`

```php
/**
 * Filter hidden fields
 *
 * @param $hidden_fields  An empty array()
 * @return array  Array with will be looped with: foreach ( $hidden_fields as $name => $value )
 */
add_filter('wpcf7_form_hidden_fields', function($hidden_fields = array()) {
    return $hidden_fields;
});
```

- `wpcf7_form_response_output`

```php
/**
 * Filter the form response output
 *
 * @param $output 
 * @param $class 
 * @param $content 
 * @param $cf7 
 * @return @output
 */
add_filter('wpcf7_form_response_output', function($output, $class, $content, $cf7) {
    return $output;
});
```

- `wpcf7_validation_error`

```php
/**
 * Return the validation HTML code message for a field error
 *
 * @param $error The HTML like '<span role="alert" class="wpcf7-not-valid-tip">%s</span>
 * @param $name The field name
 * @param $cf7 The CF7 object
 * @return @error The new HTML error
 */
add_filter('wpcf7_validation_error', function($error, $name, $cf7) {
    return $error;
});
```

- `wpcf7_form_elements`

```php
/**
 * Return all visible form elements
 *
 * @return $form_elements
 */
function filter_wpcf7_form_elements( $elements ) {     
    return $elements; 
};
add_filter( 'wpcf7_form_elements', 'filter_wpcf7_form_elements', 10, 3 ); 
```


- `wpcf7_collect_mail_tags`

```php
/**
 * Return all visible form mail tags
 *
 * @return $mailtags
 */
function filter_wpcf7_collect_mail_tags( $mailtags, $args, $cf7 ) {     
    return $mailtags;
};
add_filter( 'wpcf7_collect_mail_tags', 'filter_wpcf7_collect_mail_tags', 10, 3 ); 
```


- `wpcf7_display_message`

```php
/**
 * Return display messaged based on status
 *
 * @return $message  string with the display messages
 */
function filter_wpcf7_display_message( $message, $status ) {     
    return $message;
};
add_filter( 'wpcf7_display_message', 'filter_wpcf7_display_message', 10, 2 ); 
```


- `wpcf7_verify_nonce`

```php
/**
 * Description
 *
 * @return $is_active  boolean 
 */
function filter_wpcf7_display_message( $is_active, $cf7 ) {     
    return $is_active;
};
add_filter( 'wpcf7_verify_nonce', 'filter_wpcf7_verify_nonce', 10, 2 ); 
```


- `wpcf7_copy`

```php
/**
 * Return new copy of form
 *
 * @return $new  $cf7 class object 
 */
function filter_wpcf7_display_message( $new, $cf7 ) {     
    return $new;
};
add_filter( 'wpcf7_copy', 'filter_wpcf7_copy', 10, 2 ); 
```


- `wpcf7_contact_form_shortcode`

```php
/**
 * Return shortcode
 *
 * @return $shortcode  string  shortcode
 */
function filter_wpcf7_display_message( $shortcode, $args, $cf7 ) {     
    return $shortcode;
};
add_filter( 'wpcf7_contact_form_shortcode', 'filter_wpcf7_contact_form_shortcode', 10, 3 ); 
```

## Filters in /contact-form-7/includes/form-tag.php 

- `wpcf7_form_tag_data_option`

```php
/**
 * Return options for tag data
 *
 * @return $options  array  
 */
function filter_wpcf7_form_tag_data_option( $varx = null, $options, $args ) {     
    return $options;
};
add_filter( 'wpcf7_form_tag_data_option', 'filter_wpcf7_form_tag_data_option', 10, 3 ); 
```

## Filters in /contact-form-7/includes/form-tags-manager.php 

- `wpcf7_form_tag`

```php
/**
 * Return scanned_tag 
 *
 * @return $scanned_tag  array  
 */
function filter_wpcf7_form_tag( $scanned_tag, $replace ) {     
    return $scanned_tag;
};
add_filter( 'wpcf7_form_tag', 'filter_wpcf7_form_tag', 10, 2 ); 
```


## Filters in /contact-form-7/includes/formatting.php 


- `wpcf7_is_email`

```php
/**
 * Return if a field is an email field
 *
 * @return $result  boolean
 */
function filter_wpcf7_is_email( $result, $email ) {     
    return $result;
};
add_filter( 'wpcf7_is_email', 'filter_wpcf7_is_email', 10, 2 ); 
```

- `wpcf7_is_email`

```php
/**
 * Return if a field is an URL field
 *
 * @return $result  boolean
 */
function filter_wpcf7_is_url( $result, $url ) {     
    return $result;
};
add_filter( 'wpcf7_is_url', 'filter_wpcf7_is_url', 10, 2 ); 
```

- `wpcf7_is_tel`

```php
/**
 * Return if a field is a telephone field
 *
 * @return $result  boolean
 */
function filter_wpcf7_is_tel( $result, $tel ) {     
    return $result;
};
add_filter( 'wpcf7_is_tel', 'filter_wpcf7_is_tel', 10, 2 ); 
```


- `wpcf7_is_number`

```php
/**
 * Return if a field is a number field
 *
 * @return $result  boolean
 */
function filter_wpcf7_is_number( $result, $number ) {     
    return $result;
};
add_filter( 'wpcf7_is_number', 'filter_wpcf7_is_number', 10, 2 ); 
```

- `wpcf7_is_number`

```php
/**
 * Return if a field is a date field
 *
 * @return $result  boolean
 */
function filter_wpcf7_is_date( $result, $date ) {     
    return $result;
};
add_filter( 'wpcf7_is_date', 'filter_wpcf7_is_date', 10, 2 ); 
```
