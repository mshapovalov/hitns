---


---

<h2 id="how-to-show-current-branch-in-the-command-prompt">How to show current branch in the command prompt</h2>
<p>Open the  <code>~/.bashrc</code>  file with your favorite text editor and add the following lines:</p>
<pre><code>git_branch() {
  git branch 2&gt; /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}

export PS1="[\u@\h \W]\$(git_branch)\$ "
</code></pre>

