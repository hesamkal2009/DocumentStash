Watch OUT!!! Watch OUT!!! Watch OUT!!!
---
___chown or chmod is NOT the solution, because of security-risk.___

Instead do this, do:

First check, where npm point to, if you call:

npm config get prefix
If /usr is returned, you can do the following:

<pre>
mkdir ~/.npm-global
export NPM_CONFIG_PREFIX=~/.npm-global
export PATH=$PATH:~/.npm-global/bin
</pre>
---
This create a npm-Directory in your Home-Directory and point npm to it.

To got this changes permanent, you have to add the export-command to your .bashrc:
---
<pre>
echo -e "export NPM_CONFIG_PREFIX=~/.npm-global\nexport PATH=\$PATH:~/.npm-global/bin" >> ~/.bashrc
</pre>
