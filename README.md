buster.js version 0.2
Copyright (C) 2012 Rick Ford
http://www.spoontwisted.com/projects/buster-js/

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

busterjs readme
================

http://www.spoontwisted.com/projects/buster-js/

busterjs is a "frame buster buster" script which allows you to display pages in a frame that have "frame busters," a type of script that prevents pages from being displayed in frames. This script should not be used to misrepresent the owner of the framed page.

busterjs requires jQuery - I've tested it on 1.6.3+

Usage
================
For use with a single frame, simply call buster.wait and pass the unique ID of the frame where you want to prevent busting:

```html
<iframe src="http://vimeo.com/39408892" id="thisFrame" frameborder="0" style="width: 800px; height: 500px;"></iframe>
<script>
	$(function(){
		buster.wait("#thisFrame");
	});
</script>
```

For use with any frame on the page, call buster.wait("iframe"), which will watch every iframe on the page. Please note the performance and reliability of this may be finicky:

```html
<script>
	$(function(){
		buster.wait("iframe");
	});
</script>
```

Finally, if you want to integrate busterjs into your own app, you can simply call buster.on and buster.off as you see fit:

```javascript
buster.on();
buster.off();
```
