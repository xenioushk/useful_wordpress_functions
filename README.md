<h2>Require once for a plugin file.</h2>

<pre><code> require_once plugin_dir_path(__FILE__) . 'inc/bwloop-plugin-activate.php';</code></pre>


<h2>Enqueue script.</h2>

<pre><code>wp_enqueue_script('mypluginscript', plugins_url('/assets/myscripts.js', __FILE__), [], '1.0.0', true);</code></pre>


<h2>Enqueue Style.</h2>

<pre><code>wp_enqueue_style('mypluginstyle', plugins_url('/assets/mystyles.css', __FILE__));</code></pre>


<h2>Basic Custom Post Type.</h2>

<pre><code>register_post_type('jobs', ['public' => true, 'label' => 'Jobs']);</code></pre>


<h2>Flash Rewrite Function.</h2>

<pre><code>flush_rewrite_rules();</code></pre>

<h2>Plugin Activation Hook.</h2>

<pre><code>require_once plugin_dir_path(__FILE__) . 'inc/bwloop-plugin-activate.php';
register_activation_hook(__FILE__, ['BwloopPluginActivate', 'activate']);</code></pre>

<h2>Plugin Deactivation Hook.</h2>

<pre><code>require_once plugin_dir_path(__FILE__) . 'inc/bwloop-plugin-deactivate.php';
register_activation_hook(__FILE__, ['BwloopPluginDeactivate', 'deactivate']);</code></pre>


<h2>Other Resources: </h2>

https://developer.wordpress.org/resource/dashicons/#dismiss