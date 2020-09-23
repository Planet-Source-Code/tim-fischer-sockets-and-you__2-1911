<div align="center">

## Sockets and You


</div>

### Description

Have you ever wanted to create a chat program in Java? Well now you can with the one and only Socket!
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Tim Fischer](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/tim-fischer.md)
**Level**          |Intermediate
**User Rating**    |4.6 (32 globes from 7 users)
**Compatibility**  |Java \(JDK 1\.1\)
**Category**       |[Internet/ Browsers/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-browsers-html__2-68.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/tim-fischer-sockets-and-you__2-1911/archive/master.zip)





### Source Code

```

<style>
<!--
 /* Font Definitions */
@font-face
	{font-family:"MS Mincho";
	panose-1:0 0 0 0 0 0 0 0 0 0;
	mso-font-alt:"\FF2D\FF33 \660E\671D";
	mso-font-charset:128;
	mso-generic-font-family:roman;
	mso-font-format:other;
	mso-font-pitch:fixed;
	mso-font-signature:1 134676480 16 0 131072 0;}
@font-face
	{font-family:"\@MS Mincho";
	panose-1:0 0 0 0 0 0 0 0 0 0;
	mso-font-charset:128;
	mso-generic-font-family:roman;
	mso-font-format:other;
	mso-font-pitch:fixed;
	mso-font-signature:1 134676480 16 0 131072 0;}
 /* Style Definitions */
p.MsoNormal, li.MsoNormal, div.MsoNormal
	{mso-style-parent:"";
	margin:0in;
	margin-bottom:.0001pt;
	mso-pagination:widow-orphan;
	font-size:12.0pt;
	font-family:"Times New Roman";
	mso-fareast-font-family:"Times New Roman";}
a:link, span.MsoHyperlink
	{color:blue;
	text-decoration:underline;
	text-underline:single;}
a:visited, span.MsoHyperlinkFollowed
	{color:purple;
	text-decoration:underline;
	text-underline:single;}
p.MsoPlainText, li.MsoPlainText, div.MsoPlainText
	{margin:0in;
	margin-bottom:.0001pt;
	mso-pagination:widow-orphan;
	font-size:10.0pt;
	font-family:"Courier New";
	mso-fareast-font-family:"Times New Roman";}
@page Section1
	{size:8.5in 11.0in;
	margin:1.0in 1.25in 1.0in 1.25in;
	mso-header-margin:.5in;
	mso-footer-margin:.5in;
	mso-paper-source:0;}
div.Section1
	{page:Section1;}
-->
</style>
</head>
<body lang=EN-US link=blue vlink=purple style='tab-interval:.5in'>
<div class=Section1>
<p class=MsoNormal>It seems we meet again. Or for the first time perhaps?
Either way, I&#8217;ve come to enjoy your company. So lets talk over some Java. Remember
to include the java.net and java.io packages!</p>
<p class=MsoNormal><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></p>
<p class=MsoNormal>You want to learn about sockets? Here are there basic steps
to help that go throw the connection process:</p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'>1) Server (</span><span
style='font-size:10.0pt;mso-bidi-font-size:12.0pt;font-family:Arial;mso-fareast-font-family:
"MS Mincho";color:red'>Tim</span><span style='mso-fareast-font-family:"MS Mincho"'>)
- Creates a new socket listening on port 4444. <o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'>2)Client (</span><span
style='font-size:10.0pt;mso-bidi-font-size:12.0pt;font-family:Arial;mso-fareast-font-family:
"MS Mincho";color:red'>Chris</span><span style='mso-fareast-font-family:"MS Mincho"'>)
&#8211; Creates a new socket connecting to </span><span style='font-size:10.0pt;
mso-bidi-font-size:12.0pt;font-family:Arial;mso-fareast-font-family:"MS Mincho";
color:red'>Tim</span><span style='mso-fareast-font-family:"MS Mincho"'> on port
4444.<o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'>3) Data
transfer begins.<o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoNormal>Initializing a client socket looks like this.</p>
<p class=MsoNormal><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho"'>Socket <span style='color:navy'>clientSocket</span>
= null;<o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:navy'>clientSocket</span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho"'> = new Socket(<span
style='color:red'>&quot;Tim&quot;</span>,<span style='color:#FFCC00'> </span>4444);<o:p></o:p></span></p>
<p class=MsoNormal><span style='font-family:Arial'><span style="mso-spacerun:
yes"> </span><o:p></o:p></span></p>
<p class=MsoNormal>This socket is connecting to a computer called <span
style='font-size:10.0pt;mso-bidi-font-size:12.0pt;font-family:Arial;mso-fareast-font-family:
"MS Mincho";color:red'>Tim </span><span style='mso-fareast-font-family:"MS Mincho"'>on
port 4444. Now, </span><span style='font-size:10.0pt;mso-bidi-font-size:12.0pt;
font-family:Arial;mso-fareast-font-family:"MS Mincho";color:red'>Tim </span><span
style='mso-fareast-font-family:"MS Mincho"'>can be either the name of a
computer on a network or an IP address. But before a client connects to a
server socket, there has to <b>be </b>a server socket.<o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho"'>Socket <span style='color:navy'>serverSocket</span>
= null;<o:p></o:p></span></p>
<p class=MsoNormal style='text-indent:.5in'><span style='font-size:10.0pt;
mso-bidi-font-size:12.0pt;font-family:Arial;mso-fareast-font-family:"MS Mincho";
color:navy'>serverSocket</span><span style='font-size:10.0pt;mso-bidi-font-size:
12.0pt;font-family:Arial;mso-fareast-font-family:"MS Mincho"'> = new Socket(4444);
<span style='color:#00CC00'>//Notice no user to connect to this time.</span><o:p></o:p></span></p>
<p class=MsoNormal style='text-indent:.5in'><span style='font-size:10.0pt;
mso-bidi-font-size:12.0pt;font-family:Arial;mso-fareast-font-family:"MS Mincho";
color:navy'>serverSocket</span><span style='font-size:10.0pt;mso-bidi-font-size:
12.0pt;font-family:Arial;mso-fareast-font-family:"MS Mincho"'>.accept(); <span
style='color:#00CC00'>//Accept a client.<o:p></o:p></span></span></p>
<p class=MsoNormal><span style='font-size:10.0pt;mso-bidi-font-size:12.0pt;
font-family:Arial;mso-fareast-font-family:"MS Mincho";color:#00CC00'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'>Not too
hard is it? Now lets explain step three: Data Transfer.<o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'>From the
socket you must receive input and you must send output. Clear? Good. To do this
you must declare a <span style='color:purple'>PrintWriter</span><span
style='color:#993366'> </span>for output and a <span style='color:purple'>BufferedReader
</span>for input. The following good is used for both a client and a server
socket. For the sake of simplicity I will use a client socket.<o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:purple'>PrintWriter</span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho"'> <span
style='color:#CC0000'>out</span> = null;<o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:purple'>BufferedReader</span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho"'> <span
style='color:green'>in</span> = null;<o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho"'>Socket <span style='color:navy'>clientSocket</span>
= null;<o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:navy'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:navy'>clientSocket</span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho"'> = new Socket(<span
style='color:red'>&quot;Tim&quot;</span>,<span style='color:#FFCC00'> </span>4444);<o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:#CC0000'>out</span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho"'> = new <span
style='color:#993366'>PrintWriter</span>(<span style='color:navy'>clientSocket</span>.getOutputStream(),
true); <span style='color:#00CC00'>//get the socket&#8217;s ouput<o:p></o:p></span></span></p>
<p class=MsoPlainText style='margin-left:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:green'>in</span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho"'> = new <span
style='color:#993366'>BufferedReader</span>( new inputStreamReader( <span
style='color:navy'>clientSocket</span>.getInputStream() ) ); <span
style='color:#00CC00'>//get the socket&#8217;s input<o:p></o:p></span></span></p>
<p class=MsoPlainText style='margin-left:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho"'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoPlainText><span style='font-size:12.0pt;mso-bidi-font-size:10.0pt;
font-family:"Times New Roman";mso-fareast-font-family:"MS Mincho"'>Looking
back, I think I overdid the color. Oh well. All you really need to look at are
the last two lines. The </span><span style='font-family:Arial;mso-fareast-font-family:
"MS Mincho";color:purple'>PrintWriter</span><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho"'> <span style='color:#CC0000'>out </span></span><span
style='font-size:12.0pt;mso-bidi-font-size:10.0pt;font-family:"Times New Roman";
mso-fareast-font-family:"MS Mincho"'>will be the new front door for the
socket&#8217;s output. Calling </span><span style='font-family:Arial;mso-fareast-font-family:
"MS Mincho";color:#CC0000'>out</span><span style='font-family:Arial;mso-fareast-font-family:
"MS Mincho"'>.println(&#8220;Hello&#8221;) </span><span style='font-size:12.0pt;mso-bidi-font-size:
10.0pt;font-family:"Times New Roman";mso-fareast-font-family:"MS Mincho"'>would
send the string </span><span style='font-family:Arial;mso-fareast-font-family:
"MS Mincho"'>hello</span><span style='font-size:12.0pt;mso-bidi-font-size:10.0pt;
font-family:Arial;mso-fareast-font-family:"MS Mincho"'> </span><span
style='font-size:12.0pt;mso-bidi-font-size:10.0pt;font-family:"Times New Roman";
mso-fareast-font-family:"MS Mincho"'>to the server. Not too hard. I am going to
finish this showing you how to use a loop to receive information. <o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho"'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:purple'>PrintWriter</span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho"'> <span
style='color:#CC0000'>out</span> = null;<o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:purple'>BufferedReader</span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho"'> <span
style='color:green'>in</span> = null;<o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho"'>Socket <span style='color:navy'>clientSocket</span>
= null;<o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho"'>String fromServer;<br>
<![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:navy'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:navy'>clientSocket</span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho"'> = new Socket(<span
style='color:red'>&quot;Tim&quot;</span>,<span style='color:#FFCC00'> </span>4444);<o:p></o:p></span></p>
<p class=MsoPlainText style='margin-left:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:#CC0000'>out</span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho"'> = new <span
style='color:#993366'>PrintWriter</span>(<span style='color:navy'>clientSocket</span>.getOutputStream(),
true); <o:p></o:p></span></p>
<p class=MsoPlainText style='margin-left:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:green'>in</span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho"'> = new <span
style='color:#993366'>BufferedReader</span>(new inputStreamReader( <span
style='color:navy'>clientSocket</span>.getInputStream() ) );<o:p></o:p></span></p>
<p class=MsoPlainText style='margin-left:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho"'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoPlainText style='text-indent:.5in'><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho"'>while ((fromServer = <span
style='color:green'>in</span>.readLine()) != null) { <span style='color:#00CC00'>//Loop
while we are still getting messages</span><br>
<span style="mso-spacerun:
yes">            </span>System.out.println(&quot;Server: &quot; + fromServer); <span
style='color:#00CC00'>//Display message we got</span><br>
<span
style="mso-spacerun: yes">            </span><br>
<span style="mso-spacerun:
yes">                </span>}<o:p></o:p></span></p>
<p class=MsoPlainText><span style='font-family:Arial;mso-fareast-font-family:
"MS Mincho"'><span style='mso-tab-count:1'>            </span><o:p></o:p></span></p>
<p class=MsoPlainText><span style='font-family:Arial;mso-fareast-font-family:
"MS Mincho"'><span style='mso-tab-count:1'>            </span><span
style='color:#CC0000'>out</span></span><span style='mso-fareast-font-family:
"MS Mincho"'>.close();<br>
<span style="mso-spacerun: yes">      </span></span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho";color:green'>in</span><span
style='mso-fareast-font-family:"MS Mincho"'>.close();<br>
<span
style="mso-spacerun: yes">      </span></span><span style='font-family:Arial;
mso-fareast-font-family:"MS Mincho";color:navy'>clientSocket</span><span
style='mso-fareast-font-family:"MS Mincho"'>.close();</span><span
style='font-family:Arial;mso-fareast-font-family:"MS Mincho"'><br>
<![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-bidi-font-size:10.0pt;mso-fareast-font-family:
"MS Mincho"'>I know right now some people aren&#8217;t going to understand this
article. If you read it and don&#8217;t know how to make a chat program then you need
to read some more tutorials. I suggest going to <a href="http://java.sun.com/">http://java.sun.com/</a>
for more help. Email me with feedback type stuff &#8211; <a href="mailto:tim@bbs-la.com">Tim Fischer</a><o:p></o:p></span></p>
<p class=MsoNormal><span style='mso-fareast-font-family:"MS Mincho"'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
<p class=MsoNormal style='text-indent:.5in'><span style='color:#339966'><![if !supportEmptyParas]>&nbsp;<![endif]><o:p></o:p></span></p>
</div>
```

