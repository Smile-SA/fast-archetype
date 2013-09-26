Layout use the CSS property display with value table, table, cell, ...

As IE6 and 7 don't support it, there is a conditionnal treatment to separate those 2 from other browsers :
- good browser get div-based layout (with display:table)
- IE6 and 7 get a table layout (with table, tr and td)

If you don't support IE6 and 7, you may get rid of those layout (for the mockup' sake anyway, you may keep it into liferay template).

If you don't want to do a server side conditionnal treatment, you can use IE HTML conditionnal comment.
Instead of : 
	${symbol_pound}if (${symbol_dollar}browserSniffer.isIe(${symbol_dollar}request) && ${symbol_dollar}browserSniffer.getMajorVersion(${symbol_dollar}request) < 8)
		<table class="portlet-layout">
			<tr>
				<td class="portlet-column portlet-column-only" id="column-1">
					${symbol_dollar}processor.processColumn("column-1", "portlet-column-content portlet-column-content-only")
				</td>
			</tr>
		</table>
	${symbol_pound}else
		<div class="portlet-layout">
			<div class="portlet-column portlet-column-only" id="column-1">
				${symbol_dollar}processor.processColumn("column-1", "portlet-column-content portlet-column-content-only")
			</div>
		</div>
	${symbol_pound}end

You may write :
	<!--[if lt IE 8]>
		<table class="portlet-layout"><tr><td class="portlet-column portlet-column-only" id="column-1">
	<![endif]-->
	<!--[if gt IE 7]><!-->
		<div class="portlet-layout"><div class="portlet-column portlet-column-only" id="column-1">
	<!--<![endif]-->
		${symbol_dollar}processor.processColumn("column-1", "portlet-column-content portlet-column-content-only")
	<!--[if lt IE 8]>
		</td></tr></table>
	<![endif]-->
	<!--[if gt IE 7]><!-->
		</div></div>
	<!--<![endif]-->
