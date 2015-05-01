This is our fork of Snowplow's javscript collector.

Our fork adds an "elased time" feature to the collector:

The code keeps an elapsed time timer while the user is 
actively engaging the page. This data is sent along
in the payload. 

To roll a new version:

1. git checkout master (to ensure you are at master)
1. git branch <new branch>
2. git checkout <new branch>
3. git fetch upstream/master

At this point, you have a new branch and the newest code 
from upstream. You probably want to merge in a tagged 
version of the upstream, so look it up:

4.Find the tag you want to merge in> 

> git tag 

Our versions start with 'p' and Snowplow's don't. 

2.4.3 <== upsteam
p.2.4.3 <== local to this repo. 

5. Merge in the desired tag:

git merge <tag>

6. Fix any conflicts. 

7. Test 

> grunt test

Fix any issues.

8. 

> git commit 

9. Merge into master

> git checkout master
> git merge <new branch>

10. Tag it using the same tag as upsteram, but prepend with 'p'

> git tag p<tag>

11. Push to origin. 

> git push origin

12. Roll a new release 

> grunt




