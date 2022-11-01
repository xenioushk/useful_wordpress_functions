<h4>Require once for a plugin file.</h4>

<pre><code> require_once plugin_dir_path(__FILE__) . 'inc/bwloop-plugin-activate.php';</code></pre>


<h4>Enqueue script.</h4>

<pre><code>wp_enqueue_script('mypluginscript', plugins_url('/assets/myscripts.js', __FILE__), [], '1.0.0', true);</code></pre>


<h4>Enqueue Style.</h4>

<pre><code>wp_enqueue_style('mypluginstyle', plugins_url('/assets/mystyles.css', __FILE__));</code></pre>


<h4>Basic Custom Post Type.</h4>

<pre><code>register_post_type('jobs', ['public' => true, 'label' => 'Jobs']);</code></pre>


<h4>Flash Rewrite Function.</h4>

<pre><code>flush_rewrite_rules();</code></pre>

<h4>Plugin Activation Hook.</h4>

<pre><code>require_once plugin_dir_path(__FILE__) . 'inc/bwloop-plugin-activate.php';
register_activation_hook(__FILE__, ['BwloopPluginActivate', 'activate']);</code></pre>

<h4>Plugin Deactivation Hook.</h4>

<pre><code>require_once plugin_dir_path(__FILE__) . 'inc/bwloop-plugin-deactivate.php';
register_activation_hook(__FILE__, ['BwloopPluginDeactivate', 'deactivate']);</code></pre>

<h2>WordPress Admin Hooks.</h2>

<h4>Admin Menu Hook.</h4>

<pre><code>add_action('admin_menu', [$this, 'registerAdminMenu']);

public function registerAdminMenu()
{
  add_menu_page('BWL OOP Settings', 'BWL OOP', 'manage_options', 'bwl_oop_settings', [$this, 'bwloopSettingsTemplate'], 'dashicons-store', 100);
}

public function bwloopSettingsTemplate()
{
  echo "OOP Settings Page";
}</code></pre>


<h4>Other Resources: </h4>

https://developer.wordpress.org/resource/dashicons/#dismiss