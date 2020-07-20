# xymon_new_design
Design Update from Xymon 4.3.30 (graphics, CSS etc.)

<img src="https://raw.githubusercontent.com/Sabo86/xymon_new_design/master/xymon_new_design.png" style="max-width:100%;">



###### First step: 
- Download Xymon (https://sourceforge.net/projects/xymon/)

###### Step two:
- install Xymon as described here (https://xymon.sourceforge.io/xymon/help/install.html)

###### Step three:
- Now Xymon should be installed and running
- To customize the graphic change to the folder where you unzipped Xymon (first step)
- ~/xymon-4.3.30/xymongen you copy the file pagegen.c 
- Of course you can adjust the pagegen.c before
- Now you execute "make" and "make install" again as described in "Building Xymon

###### Step four:
1. store graphics 
  - Create a new folder under ~./server/www/gifs with the name new
  - Unpack the file graphics.zip in the folder new
2. Store xymonbody.css and xymonmenu-new.css
  - Copy the xymonbody.css into the folder ~./server/www/gifs/new/
  - Copy the xymonmenu-new.css into the folder ~./server/www/menu/
3. enter everything in the ~./server/etc/xymonserver.cfg
  - Modify the following lines in xymonserver.cfg:
  
  XYMONSKIN="$XYMONSERVERWWURL/gifs/new"	  
  XYMONBODYMENUCSS="$XYMONMENUSKIN/xymonmenu-new.css"



###### Step five:
- ~/server/web/ customize footer and header files

###### e.g. standard stdnormal_header fileo:

`` `
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN">
<HTML>
<HEAD>
<META HTTP-EQUIV="Content-Type" CONTENT="&HTMLCONTENTTYPE">
<META HTTP-EQUIV="REFRESH" CONTENT="&XYMWEBREFRESH">
<META HTTP-EQUIV="EXPIRES" CONTENT="Sat, 01 Jan 2001 00:00:00 GMT">
<META HTTP-EQUIV="Set-Cookie" CONTENT="pagepath=&XYMWEBPAGEPATH; path=/">
<META HTTP-EQUIV="Set-Cookie" CONTENT="host=; path=/">
<TITLE>&XYMWEBBACKGROUND : Xymon - Status @ &XYMWEBDATE</TITLE>

<!-- Styles for the Xymon body  -->
<link rel="stylesheet" type="text/css" href="&XYMONBODYCSS">

<!-- Styles for the menu bar -->
<link rel="stylesheet" type="text/css" href="&XYMONBODYMENUCSS">

<!-- The favicon image -->
<link rel="shortcut icon" href="&XYMONSKIN/favicon-&XYMWEBBACKGROUND.ico">
<link rel="stylesheet" type="text/css" href="/xymon/gifs/static/xymonbody.css">
</HEAD>

<BODY class="&XYMWEBBACKGROUND">

&XYMONBODYHEADER

<div class="webpage_header">
	
		<TABLE SUMMARY="Topline" WIDTH="100%">
		<TR>
		  <TD VALIGN=MIDDLE ALIGN=LEFT WIDTH="30%">
		   <B>&nbsp; &XYMONLOGO </B>
		  </TD>
		  <TD VALIGN=MIDDLE ALIGN=CENTER WIDTH="40%">
			<B>Current Status</B>
		  </TD>
		  <TD VALIGN=MIDDLE ALIGN=RIGHT WIDTH="30%">
		   <B> &XYMWEBDATE &nbsp;</B>
		  </TD>
		</TR>
		<TR>
		  
		</TR>
		</TABLE>
</div>		
`` `

###### Adapted file:
<code>
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0//EN">
<HTML>
<HEAD>
<META HTTP-EQUIV="Content-Type" CONTENT="&HTMLCONTENTTYPE">
<META HTTP-EQUIV="REFRESH" CONTENT="&XYMWEBREFRESH">
<META HTTP-EQUIV="EXPIRES" CONTENT="Sat, 01 Jan 2001 00:00:00 GMT">
<META HTTP-EQUIV="Set-Cookie" CONTENT="pagepath=&XYMWEBPAGEPATH; path=/">
<META HTTP-EQUIV="Set-Cookie" CONTENT="host=; path=/">
<TITLE>&XYMWEBACKGROUND : Xymon - Status @ &XYMWEBDATE</TITLE>
<!-- Styles for the Xymon body -->
<link rel="stylesheet" type="text/css" href="&XYMONBODYCSS">
<!-- Styles for the menu bar -->
<link rel="stylesheet" type="text/css" href="&XYMONBODYMENUCSS">
<!-- The favicon image -->
<link rel="shortcut icon" href="&XYMONSKIN/favicon-&XYMWEBBACKGROUND.ico">
<link rel="stylesheet" type="text/css" href="/xymon/gifs/new/xymonbody.css">
</HEAD>

<BODY class="&XYMWEBBACKGROUND">

&XYMONBODYHEADER
</code>
<div class="webpage_header">
	
		<TABLE SUMMARY="Topline" WIDTH="100%">
		<TR>
		  <TD VALIGN=MIDDLE ALIGN=LEFT WIDTH="30%">
		   <B>&nbsp; &XYMONLOGO </B>
		  </TD>
		  <TD VALIGN=MIDDLE ALIGN=CENTER WIDTH="40%">
			<B>Current Status</B>
		  </TD>
		  <TD VALIGN=MIDDLE ALIGN=RIGHT WIDTH="30%">
		   <B> &XYMWEBDATE &nbsp;</B>
		  </TD>
		</TR>
		<TR>
		  
		</TR>
		</TABLE>
</div>		
<br>

