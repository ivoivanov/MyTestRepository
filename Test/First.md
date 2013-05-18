<!DOCTYPE html>
<html>
	<head>
		<title>Title of the document</title>
	</head>

	<body>


</html>

<div style="DISPLAY: none">
	<input name="userDataCache" type="hidden" class="userDataStyle" id="userDataCache" />
	<input name="hiddenScrollOffset" type="hidden" id="hiddenScrollOffset" />
</div>
<img name="collapseImage" style="DISPLAY: none; WIDTH: 0px; HEIGHT: 0px" id="collapseImage" src="images/collapse.gif" />
<img name="expandImage" style="DISPLAY: none; WIDTH: 0px; HEIGHT: 0px" id="expandImage" src="images/expand.gif" />
<img name="copyImage" style="DISPLAY: none; WIDTH: 0px; HEIGHT: 0px" id="copyImage" src="images/copycode.gif" />
<img name="copyHoverImage" style="DISPLAY: none; WIDTH: 0px; HEIGHT: 0px" id="copyHoverImage" src="images/copycodeHighlight.gif" />

<div id="pagetop">


	<table width="100%" id="pagetoptable1">
		<tbody>


			<tr id="pagetoptable1row2">
				<td align="left" colspan="2">
					<span id="pagetitle">How to: Bind Data to ASP.NET Controls</span>
				</td>
			</tr>

		</tbody>
	</table>
</div>

<div class="hspopupbubble" id="hsglossaryitembox">
	<p>Glossary Item Box</p>
</div>

<div id="pagebody">
	<div id="mainbody">
		<p>
			Telerik OpenAccess ORM enables you to bind ASP.NET controls such as <strong>RadComboBox</strong> and <strong>RadGrid</strong>.
		</p>
		<h1>Adding RadScriptManager</h1>
		<p>
			The first step when you want to use RadControls for ASP.NET AJAX is to add a <strong>RadScriptManager</strong>. By default each of the RadControls for ASP.NET Ajax serves a set of files (JS code) needed for its proper client-side operation. When loading a page with several controls on it, the number of these files can become very large, often resulting in a reduced page load time and increased traffic. The reason for this problem is that browsers make a separate request to the server for each of these resources. With the newly added <strong>RadScriptManager</strong> control, RadControls for ASP.NET Ajax suite gives developers the advantage of a simple drag-and-drop to achieve the combination of resources to a single request. All you need is to add a <strong>RadScriptManager</strong> to your page and the javascript files get combined into a single file.
		</p>
		<p>
			Open your page in Design mode. Drag a new <strong>RadScriptManager</strong> component from the <strong>Toolbox</strong> to the designer.
		</p>
		<p>
			<img border="0" src="images/1DevGuide-IntegrTelerikProducts-AspNet-DataBind-010.png" alt="" />
		</p>
		<p>
			<strong>RadScriptManager</strong> needs an <strong>HttpHandler</strong> to be declared in the application configuration file to operate properly. The addition of the handler is made easy by the <strong>SmartTags</strong> of the control. Right-click the <strong>RadScriptManager</strong> and select <strong>Show Smart Tag</strong>. Then select <strong>Register Telerik.Web.UI.WebResource.axd</strong>.
		</p>
		<h1>Binding Data to RadControls for ASP.NET AJAX</h1>
		<p>
			You can bind object using the code-behind method as well. You can easily do this by retrieving all the objects that you wish to bind and by taking advantage of the <strong>DataSource</strong> property of the control to which you wish to bind the result set. The following example shows how to retreive a single column from a data table and bind it to a&amp;nbsp;<strong>RadComboBox</strong>.
		</p>
		<div class="LanguageSpecific" id="Syntax_CS">
			<table cellpadding="0" width="100%" cellspacing="0" class="syntaxtable">
				<tbody>
					<tr>
						<th>C#</th>
						<th>
							<span class="hs-onlineonly">
								<span onmouseover="changeCopyCodeIcon(this,true)" onclick="copyCode(this)" class="copyCode" onmouseout="changeCopyCodeIcon(this,false)" onkeypress="CopyCode_CheckKey(this)" onfocusin="changeCopyCodeIcon(this,true)" onfocusout="changeCopyCodeIcon(this,false)" tabindex="0">
									<img name="ccImage" align="absMiddle" class="copyCodeImage" src="images/copycode.gif" />Copy Code
								</span>
							</span>
						</th>
					</tr>
					<tr>
						<td colspan="2">
							<div class="colorizedcode">
								<font color="blue">using</font>
								<font color="black">(EntitiesModel dbContext =</font>
								<font color="blue">new</font>
								<font color="black">
									EntitiesModel())<br />{<br />&amp;nbsp;&amp;nbsp;&amp;nbsp;RadComboBox.DataSource = dbContext.Categories.ToList();<br />&amp;nbsp;&amp;nbsp;&amp;nbsp;RadComboBox.DataTextField =
								</font>
								<font color="#a31515">&quot;CategoryName&quot;</font>
								<font color="black">
									;<br />&amp;nbsp;&amp;nbsp;&amp;nbsp;RadComboBox.DataBind();<br />}
								</font>
							</div>
						</td>
					</tr>
				</tbody>
			</table>
		</div>
		<div class="LanguageSpecific" id="Syntax_VB.NET">
			<table cellpadding="0" width="100%" cellspacing="0" class="syntaxtable">
				<tbody>
					<tr>
						<th>VB.NET</th>
						<th>
							<span class="hs-onlineonly">
								<span onmouseover="changeCopyCodeIcon(this,true)" onclick="copyCode(this)" class="copyCode" onmouseout="changeCopyCodeIcon(this,false)" onkeypress="CopyCode_CheckKey(this)" onfocusin="changeCopyCodeIcon(this,true)" onfocusout="changeCopyCodeIcon(this,false)" tabindex="0">
									<img name="ccImage" align="absMiddle" class="copyCodeImage" src="images/copycode.gif" />Copy Code
								</span>
							</span>
						</th>
					</tr>
					<tr>
						<td colspan="2">
							<div class="colorizedvbcode">
								<font class="keyword">Using</font> dbContext <font class="keyword">As</font> <font class="keyword">New</font> EntitiesModel()<br />&amp;nbsp;RadComboBox.DataSource = dbContext.Categories.ToList()<br />&amp;nbsp;RadComboBox.DataTextField = <font class="string">&quot;CategoryName&quot;</font><br />&amp;nbsp;RadComboBox.DataBind()<br /><font class="keyword">End</font> <font class="keyword">Using</font>
							</div>
						</td>
					</tr>
				</tbody>
			</table>
		</div>
		<h1>Next Step</h1>
		<p>For more information, please refer to:</p>
		<ul>
			<li>
				<a href="getting-started-root-quickstart-aspnet-overview.html">Quickstart - ASP.NET Web Application</a>
				<li>
					<a href="quickstart-asp-web-site-overview.html">Quickstart - ASP.NET Web Site</a>
					<li>
						<a style="auto-update-caption: true" href="developer-guide-integr-telerik-products-asp-ajax-use-oadatasource.html">How to: Use OpenAccessLinqDataSource in ASP.NET Applications</a>
					</li>
				</li>
			</li>
		</ul>
		<a name="seealsobookmark" id="seealsobookmark"></a>

	</div>

	<div id="pagefooter">
		<p>&amp;nbsp;</p>
		<p>&amp;nbsp;</p>
		<hr style="height: 1px" />
		<p>&amp;copy; 2002-2013 Telerik. All Rights Reserved.</p>
	</div>
</div>

</body>