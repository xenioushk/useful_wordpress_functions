<h2>Require once for a plugin file.</h2>

<pre><code>require_once plugin_dir_path(**FILE**) . 'inc/bwloop-plugin-deactivate.php';</code></pre>


<h2>Enqueue script.</h2>

<pre><code>wp_enqueue_script('mypluginscript', plugins_url('/assets/myscripts.js', __FILE__), [], '1.0.0', true);</code></pre>


<h2>Enqueue Style.</h2>

<pre><code>wp_enqueue_style('mypluginstyle', plugins_url('/assets/mystyles.css', __FILE__));</code></pre>


<h2>Basic Custom Post Type.</h2>

<pre><code>register_post_type('jobs', ['public' => true, 'label' => 'Jobs']);</code></pre>


<h2>Flash Rewrite Function.</h2>

<pre><code>flush_rewrite_rules();</code></pre>

