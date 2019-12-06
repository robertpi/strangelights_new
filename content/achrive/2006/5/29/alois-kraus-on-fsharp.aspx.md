---
title: "Alois Kraus on F#"
date: 2006-05-29T23:59:00.0000000
draft: false
---

<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><FONT face=Verdana>Alois Kraus just made <A href="http://geekswithblogs.net/akraus1/articles/79880.aspx">this nice post about functional programming</A> in F# and C#. I enjoyed the article very much and he even bigs up one of my own posts, which of course tickled me.<?xml:namespace prefix = o ns = "urn:schemas-microsoft-com:office:office" /><o:p></o:p></FONT></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><FONT face=Verdana>However, I disagree with quite a lot of what he said in his conclusion paragraph. He writes:<o:p></o:p></FONT></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><FONT face=Verdana>&#8220;<I style="mso-bidi-font-style: normal">Not all concepts of functional languages should be explored by Mort and Elvis since most of them are fairly complex to understand because functional languages are very picky (just like unix) who can be their friend and who not. If Einstein does write a F# program then only a true Einstein can maintain it. When the outsourced Mort and Elvis do change his code I am sure they will screw it up</I>&#8221;<o:p></o:p></FONT></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><FONT face=Verdana>Mort, Elvis and Einstein are different type of programmers characterized in <A href="http://www.nikhilk.net/Personas.aspx">this blog post</A> by Nikhil Kothari.<o:p></o:p></FONT></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><FONT face=Verdana>I maybe being picky here as Alois doesn&#8217;t say this directly, but he seems to imply that functional programming is more complicated than imperative/object oriented programming. <o:p></o:p></FONT></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><FONT face=Verdana>I think here he is mixing up two subtly different things, the complexity of a language and the complexity of problem a program is try to address. If the problem is sufficiently hard then it is going to be difficult to understand what ever language it is written in. I agree that the two issues are related as the design of language can make a problem harder or easier to understand when expressed in code.<o:p></o:p></FONT></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><FONT face=Verdana>So I feel his framing of function programming as more complex is a little unfair. In fact F# aims to be a good bit simpler that C# and in my opinion it succeeds because to write a program in F# one needs to understand few concepts that in C#. <o:p></o:p></FONT></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><FONT face=Verdana>To see this, let&#8217;s take a look at a simplest example we can, the hello world program.<o:p></o:p></FONT></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><FONT face=Verdana><SPAN lang=FR style="FONT-SIZE: 10pt; mso-ansi-language: FR">Version</SPAN><SPAN lang=FR style="FONT-SIZE: 10pt"> </SPAN><SPAN style="FONT-SIZE: 10pt">F#<o:p></o:p></SPAN></FONT></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana><SPAN style="FONT-WEIGHT: normal; FONT-SIZE: 11px; COLOR: black; FONT-FAMILY: Lucida Console; BACKGROUND-COLOR: transparent"><SPAN style="FONT-WEIGHT: normal; FONT-SIZE: 11px; COLOR: blue; FONT-FAMILY: Lucida Console; BACKGROUND-COLOR: transparent">do</SPAN> print_endline <SPAN style="FONT-WEIGHT: normal; FONT-SIZE: 11px; COLOR: red; FONT-FAMILY: Lucida Console; BACKGROUND-COLOR: transparent">"hello world"</SPAN></SPAN>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><FONT face=Verdana>Version C#<o:p></o:p></FONT></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana><SPAN style="FONT-WEIGHT: normal; FONT-SIZE: 11px; COLOR: black; FONT-FAMILY: Lucida Console; BACKGROUND-COLOR: transparent"><SPAN style="FONT-WEIGHT: normal; FONT-SIZE: 11px; COLOR: blue; FONT-FAMILY: Lucida Console; BACKGROUND-COLOR: transparent">class</SPAN> Prog<BR>{<BR>&nbsp;<SPAN style="FONT-WEIGHT: normal; FONT-SIZE: 11px; COLOR: blue; FONT-FAMILY: Lucida Console; BACKGROUND-COLOR: transparent">static</SPAN> <SPAN style="FONT-WEIGHT: normal; FONT-SIZE: 11px; COLOR: blue; FONT-FAMILY: Lucida Console; BACKGROUND-COLOR: transparent">int</SPAN> main()<BR>&nbsp;{<BR>&nbsp;&nbsp;System.Console.WriteLine(<SPAN style="FONT-WEIGHT: normal; FONT-SIZE: 11px; COLOR: #666666; FONT-FAMILY: Lucida Console; BACKGROUND-COLOR: #e4e4e4">"hello world"</SPAN>);<BR>&nbsp;&nbsp;<SPAN style="FONT-WEIGHT: normal; FONT-SIZE: 11px; COLOR: blue; FONT-FAMILY: Lucida Console; BACKGROUND-COLOR: transparent">return</SPAN> 0;<BR>&nbsp;}<BR><BR>}</SPAN><BR>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><FONT face=Verdana>In the F# version we need to understand just three pieces of text &#8220;do&#8221; a keyword for calling functions, &#8220;print_endline&#8221; a function from the built in libraries, and &#8220;hello world&#8221; a string literal.<o:p></o:p></FONT></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><FONT face=Verdana>The C# is more complicated. First of all we forced to define a class &#8220;Prog&#8221;, even though it does not server any purpose in this case. Next we define a method &#8220;main&#8221;; &#8220;main&#8221; is a static method meaning that doesn&#8217;t belong to any instance of the class we have defined. This static method is a special method, because it is called main and is static; it is the entry point to the program. Next comes our method body definition made up of a call to a method &#8220;WriteLine&#8221; in the class &#8220;Console&#8221; in the namespace &#8220;System&#8221;. Finally we state that we&#8217;ll return the literal &#8220;0&#8221; to the calling function. Well not quite finally as we need to remember to close all those curly brackets we opened along the way.<o:p></o:p></FONT></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><o:p><FONT face=Verdana>&nbsp;</FONT></o:p></SPAN></P>
<P class=NormalVerdana style="MARGIN: 0in 0in 0pt"><SPAN style="FONT-SIZE: 10pt"><FONT face=Verdana>I really hope Alois continues his exploration of F# and functional programming in general. <o:p></o:p></FONT></SPAN></P>

### Feedback:

*Feedback was imported from my only blog engine, it's no longer possible to post feedback here.*

**re: Alois Kraus on F# - DeeJay**

Very valid argument, and interestingly one typically used in advocation of languages such as python or ruby. In essence requiring too many concepts for achieving simple things.

**re: Alois Kraus on F# - Alois Kraus**

Hi Robert I have posted my answer here:
