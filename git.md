---


---

<h2 id="how-to-show-current-branch-in-the-command-prompt">How to show current branch in the command prompt</h2>
<p>Open the  <code>~/.bashrc</code>  file with your favorite text editor and add the following lines:</p>
<pre><code>parse_git_branch() {
     git branch 2&gt; /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "
</code></pre>
<p>Load the  <code>~/.bashrc</code>  to apply changes for the current session without login/logout:</p>
<pre><code>$ source ~/.bashrc
</code></pre>

