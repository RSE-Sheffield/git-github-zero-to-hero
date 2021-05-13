---
title: Git
weight: 5
---

Follow the installation instructions according to your system:

 ### Windows 
<a href="https://www.youtube.com/watch?v=339AEqk9c-8">Video Tutorial</a>
<ol>
<li>Download the Git for Windows <a href="https://git-for-windows.github.io/">installer</a>.</li>
<li>Run the installer and follow the steps bellow:
<ol>
<li>Click on "Next".</li>
<!-- Select Components -->
<li>Click on "Next".</li>
<!-- Adjusting your PATH environment -->
<li>
<strong>
Keep "Use Git from the Windows Command Prompt" selected and click on "Next".
</strong>
If you forgot to do this programs that you need for the workshop will not work properly. If this happens rerun the installer and select the appropriate option.
</li>
<!-- Choosing the SSH executable -->
<li>Click on "Next".</li>
<!-- Configuring the line ending conversions -->
<li>
<strong>
Keep "Checkout Windows-style, commit Unix-style line endings" selected and click on "Next".
</strong>
</li>
<!-- Configuring the terminal emulator to use with Git Bash -->
<li>
<strong>
Keep "Use Windows' default console window" selected and click on "Next".
</strong>
</li>
<!-- Configuring experimental performance tweaks -->
<li>Click on "Install".</li>
<!-- Installing -->
<!-- Completing the Git Setup Wizard -->
<li>Click on "Finish".</li>
</ol>
</li>
<li>
If your "HOME" environment variable is not set (or you don't know what this is):
<ol>
<li>Open command prompt (Open Start Menu then type <code>cmd</code> and press [Enter])</li>
<li>
Type the following line into the command prompt window exactly as shown:
<p><code>setx HOME "%USERPROFILE%"</code></p>
</li>
<li>Press [Enter], you should see <code>SUCCESS: Specified value was saved.</code></li>
<li>Quit command prompt by typing <code>exit</code> then pressing [Enter]</li>
</ol>
</li>
</ol>
<p>This will provide you with both Git and Bash in the Git Bash program.</p>




### Mac OS X

<a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">Video Tutorial</a>
<p>
<strong>For OS X 10.9 and higher</strong>, install Git for Mac
by downloading and running the most recent "mavericks" installer from
<a href="http://sourceforge.net/projects/git-osx-installer/files/">this list</a>.
After installing Git, there will not be anything in your <code>/Applications</code> folder,
as Git is a command line program.
<strong>For older versions of OS X (10.5-10.8)</strong> use the
most recent available installer labelled "snow-leopard"
<a href="http://sourceforge.net/projects/git-osx-installer/files/">available here</a>.
</p>


### Linux
<p>
If Git is not already available on your machine you can try to
install it via your distro's package manager. For Debian/Ubuntu run
<code>sudo apt-get install git</code> and for Fedora run
<code>sudo yum install git</code>.
</p>




