---


---

<h3 id="stop-all-containers">Stop all containers</h3>
<pre><code>docker stop $(docker ps -a -q)
</code></pre>
<h3 id="remove-all-containers">Remove all containers</h3>
<pre><code>docker rm $(docker ps -a -q)
</code></pre>

