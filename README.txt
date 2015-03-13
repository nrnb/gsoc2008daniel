submitted code sample for Daniel Abel's GSoC 2008 project
=========================================================
mentor org: GenMAPP
project title: Implement long-standing cytoscape wishlist features in
	cytoscape core

During the project, I used the cytoscape3/branches/abeld-gsoc/
directory of the cytoscape subversion repository, but made small fixes
directly on the cytoscape 3.0 trunk (cytoscape3/trunk) as well. All
checkins by me were done with the 'abeld' username.
The cytocape repository is at http://chianti.ucsd.edu/svn/ for more
info see http://www.cytoscape.org/cgi-bin/moin.cgi/SVN_Access

Documentation about the code I produced is available at
http://www.cytoscape.org/cgi-bin/moin.cgi/DanielAbel/EdgeDirectionality
and
http://www.cytoscape.org/cgi-bin/moin.cgi/DanielAbel/PluggableRenderers

Note that instead of reading the contents of this directory, I think
doing an 
svn log http://chianti.ucsd.edu/svn/cytoscape3/branches/abeld-gsoc
is a much better way to get an overview of the code I produced.

Contents:
=========

edge_directionality.diff
------------------------
contains the patch that was merged into
cytoscape3.0 trunk in svn revision r14560, this file was produced by:
svn diff -c14560 svn+ssh://grenache.ucsd.edu/cellar/common/svn/cytoscape3/trunk > edge_directionality.diff

smaller_fixes/
-------------
contains small bugfixes that I directly checked in into
trunk. Each fix_number.diff file contains the svn diff of checkin
'number'. These were produced with:
for i in 14572 14563 14321 14311 14310 13971; do svn diff -c$i svn+ssh://grenache.ucsd.edu/cellar/common/svn/cytoscape3/trunk > smaller_fixes/fix_$i.diff; done;

pluggable_renderers.diff
------------------------
contains the status of the second half of my GSoC project, as of
aug. 18. This project is still far from finished (although I made
great progress during the summer). The code is under
cytoscape3/branches/abeld-gsoc/dev/pluggable-renderers in the
subversion repository, and I did manage to get some work done after
aug. 18, so the included .diff is not current state of the code. (As
per google's guidelines, I am submitting the code as it was on
aug. 18.) Note that this is a refactoring project, and most of the
contents of the .diff is code that was removed.  The file was produced
with:
svn diff svn+ssh://grenache.ucsd.edu/cellar/common/svn/cytoscape3/trunk@14573  svn+ssh://grenache.ucsd.edu/cellar/common/svn/cytoscape3/branches/abeld-gsoc/dev/pluggable-renderers@14700 > pluggable_renderers.diff
