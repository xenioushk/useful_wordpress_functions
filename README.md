#Require once for a plugin file.

require_once plugin_dir_path(**FILE**) . 'inc/bwloop-plugin-deactivate.php';


#Enqueue script.

wp_enqueue_script('mypluginscript', plugins_url('/assets/myscripts.js', __FILE__), [], '1.0.0', true);


#Enqueue Style.

wp_enqueue_style('mypluginstyle', plugins_url('/assets/mystyles.css', __FILE__));


#Basic Custom Post Type.
register_post_type('jobs', ['public' => true, 'label' => 'Jobs']);


#Flash Rewrite Function.
flush_rewrite_rules();

