---
title: get_pageCount()
page_title: get_pageCount() | UI for ASP.NET AJAX Documentation
description: get_pageCount()
slug: grid/client-side-programming/gridtableview-object/properties/get_pagecount()
tags: get_pagecount()
published: True
position: 14
---

# get_pageCount()



## 

Returns the page count for the respective __GridTableView__ object. Can be used to create some condition for executing different script logic depending on how many pages the user sees.

````ASPNET
	        <telerik:RadGrid ID="RadGrid1" runat="server" AllowPaging="True"
	            OnNeedDataSource="RadGrid1_NeedDataSource">
	            <MasterTableView DataKeyNames="OrderID">
	            </MasterTableView>
	        </telerik:RadGrid>
	        <br />
	        <asp:Button ID="Button1" runat="server" Text="Click"
	            OnClientClick="buttonClick(); return false;" />
````



````JavaScript
	            function buttonClick() {
	                var grid = $find('<%= RadGrid1.ClientID %>');
	                var masterTableView = grid.get_masterTableView();
	
	                var pageCount = masterTableView.get_pageCount();
	                alert(pageCount);
	            }
````

