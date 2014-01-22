# 3D Drop In Notifier Panel #

*Description:* 3D Notifier lets you broadcast important information to your visitors using a drop down panel that appears at the top of the page. It gently scrolls the page to the top before revealing the panel in a 3D fashion. The panel contents can either be defined inline on the page, or entirely inside an external file and fetched via Ajax. Two modes of appearing are supported- "manual", where you explicitly open/close the panel, or automatic, where the panel appears automatically once per browser session to each visitor.

## Directions ##

*Step 1:* This script uses the following external files:

+ jQuery 1.10 or above (served via Google CDN)
+ notifier.js
+ notifier.css
+ content.txt

*Step 2:* Add the below code to the HEAD section of your page:

	<link rel="stylesheet" type="text/css" href="notifier.css" />
	
	<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
	
	<script src="notifier.js">
	/***********************************************
	* 3D Drop In Notifier Panel- (c) Dynamic Drive DHTML code library (www.dynamicdrive.com)
	* This notice MUST stay intact for legal use
	* Visit Dynamic Drive at http://www.dynamicdrive.com/ for this script and 100s more
	***********************************************/
	</script>
	
	<script type="text/javascript">
	
	jQuery(function(){
		notifier.init({
			noteid: 'mynotify', //id of main panel div
			content: 'content.txt', // 'inline' or 'path to external file'
			defaultstate: 'open', // 'open' or 'closed'
			freq: 'manual', //'manual' or 'session'
			oninit: function($el, state){
				// do something when panel loads
			},
			onopenclose: function($el, state){
				// do something when panel opens or closes
			}
		})
	})
	
	</script>


*Step 3:* Then, add the below sample markup to your page:

	<a href="#" class="toggle" onClick="notifier.toggle(); return false">Toggle Panel</a> <a href="#" class="toggle" onClick="notifier.open(); return false">Open</a> <a href="#" class="toggle" onClick="notifier.close(); return false">Close</a>

## 3D Drop In Notifier Panel set up ##

See script project page for additional details on setup and documentation: <http://www.dynamicdrive.com/dynamicindex17/notifier.htm>
