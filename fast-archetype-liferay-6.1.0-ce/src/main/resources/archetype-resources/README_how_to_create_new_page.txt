How to create a new page (example from src/main/resources/pages/01_web_content_display.html) :

- create a new page descriptor into src/main/resources/pages

- set skeleton and page title :

<!--${symbol_dollar}includetemplate${symbol_dollar}modules${symbol_dollar}skeleton.html${symbol_dollar}-->
	<!--${symbol_dollar}beginput${symbol_dollar}title${symbol_dollar}-->PAGE TITLE<!--${symbol_dollar}endput${symbol_dollar}-->
	<!--${symbol_dollar}beginput${symbol_dollar}mainContent${symbol_dollar}-->
		MAIN CONTENT
	<!--${symbol_dollar}endput${symbol_dollar}-->
<!--${symbol_dollar}endincludetemplate${symbol_dollar}-->

- set "main content" section with a layout (choose from src/main/resources/modules/layouttpl) :

		<!--${symbol_dollar}includetemplate${symbol_dollar}modules${symbol_dollar}layouttpl/custom/2_columns_i.html${symbol_dollar}-->
			<!--${symbol_dollar}beginput${symbol_dollar}column1${symbol_dollar}-->
				CONTENT
			<!--${symbol_dollar}endput${symbol_dollar}-->
			<!--${symbol_dollar}beginput${symbol_dollar}column2${symbol_dollar}-->
				CONTENT
			<!--${symbol_dollar}endput${symbol_dollar}-->
		<!--${symbol_dollar}endincludetemplate${symbol_dollar}-->

- set "content" section by adding new portlet

How to add new portlet

- choose a portlet skeleton (choose from src/main/resources/modules/portal/portlet_*) and set title, class (optionnal), and content :

				<!--${symbol_dollar}includetemplate${symbol_dollar}modules${symbol_dollar}portal/portlet_border.html${symbol_dollar}-->
					<!--${symbol_dollar}beginput${symbol_dollar}title${symbol_dollar}-->Web Content Display with border<!--${symbol_dollar}endput${symbol_dollar}-->
					<!--${symbol_dollar}beginput${symbol_dollar}classAddon${symbol_dollar}-->portlet-journal-content<!--${symbol_dollar}endput${symbol_dollar}-->
					<!--${symbol_dollar}beginput${symbol_dollar}body${symbol_dollar}-->
						PORTLET CONTENT
					<!--${symbol_dollar}endput${symbol_dollar}-->
				<!--${symbol_dollar}endincludetemplate${symbol_dollar}-->

- set "portlet content" section by choosing a portlet from src/main/resources/modules/portlet : 
						<!--${symbol_dollar}includetemplate${symbol_dollar}modules${symbol_dollar}portlet/webcontentdisplay.html${symbol_dollar}--><!--${symbol_dollar}endincludetemplate${symbol_dollar}-->
				