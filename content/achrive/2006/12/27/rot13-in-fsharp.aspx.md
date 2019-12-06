---
title: "ROT13 in F#"
date: 2006-12-27T07:05:00.0000000
draft: false
---

<FONT face=Arial>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 10pt; FONT-FAMILY: Arial; mso-ansi-language: EN-GB">Over on his blog, Andrei Formiga has a series of post on implementing ROT13 in F# and Haskell.<?xml:namespace prefix = o ns = "urn:schemas-microsoft-com:office:office" /><o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 10pt; FONT-FAMILY: Arial; mso-ansi-language: EN-GB"><A href="http://codemiscellany.blogspot.com/2006/12/rot13-in-f.html"><FONT color=#800080>http://codemiscellany.blogspot.com/2006/12/rot13-in-f.html</FONT></A><o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 10pt; FONT-FAMILY: Arial; mso-ansi-language: EN-GB"><A href="http://codemiscellany.blogspot.com/2006/12/rot13-in-haskell.html"><FONT color=#800080>http://codemiscellany.blogspot.com/2006/12/rot13-in-haskell.html</FONT></A><o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 10pt; FONT-FAMILY: Arial; mso-ansi-language: EN-GB"><A href="http://codemiscellany.blogspot.com/2006/12/rot13-in-f-revisited.html"><FONT color=#800080>http://codemiscellany.blogspot.com/2006/12/rot13-in-f-revisited.html</FONT></A><o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 10pt; FONT-FAMILY: Arial; mso-ansi-language: EN-GB"><A href="http://codemiscellany.blogspot.com/2006/12/still-more-rot13.html"><FONT color=#800080>http://codemiscellany.blogspot.com/2006/12/still-more-rot13.html</FONT></A><o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 10pt; FONT-FAMILY: Arial; mso-ansi-language: EN-GB"><o:p>&nbsp;</o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 10pt; FONT-FAMILY: Arial; mso-ansi-language: EN-GB">I like is implementation using library functions that don&#8217;t yet exist in F#, such as drop and zip. Here is the implementation itself, stripped of the extra library functions he had to implement, for the original see the above links. <o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="mso-ansi-language: EN-GB"><o:p><FONT face="Times New Roman">&nbsp;</FONT></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 9pt; FONT-FAMILY: 'Courier New'; mso-ansi-language: EN-GB">#light<o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 9pt; FONT-FAMILY: 'Courier New'; mso-ansi-language: EN-GB">let rot13 s = <BR><SPAN style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp; </SPAN>let letters = ['a' .. 'z']<BR><SPAN style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp; </SPAN>let transp = zip letters ((drop 13 letters) @ (take 13 letters))<BR><SPAN style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp; </SPAN>let rotchar c = List.assoc c transp<BR><SPAN style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp; </SPAN>strmap rotchar s<o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="mso-ansi-language: EN-GB"><o:p><FONT face="Times New Roman">&nbsp;</FONT></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 10pt; FONT-FAMILY: Arial; mso-ansi-language: EN-GB">The clever bit of this implementation is on the 4<SUP>th</SUP> line where he uses the functions drop and take to create a rotated list and the function zip to a map between that and the original letter list. While this is an interesting way of implementing this I think there is a way to do this without the need to define extra library functions. So here is my implementation, the same number of lines but more characters!<o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="mso-ansi-language: EN-GB"><o:p><FONT face="Times New Roman">&nbsp;</FONT></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 9pt; FONT-FAMILY: 'Courier New'; mso-ansi-language: EN-GB">#light<o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 9pt; FONT-FAMILY: 'Courier New'; mso-ansi-language: EN-GB">let rot13 (s : string) =<SPAN style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp; </SPAN><o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 9pt; FONT-FAMILY: 'Courier New'; mso-ansi-language: EN-GB"><SPAN style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp; </SPAN>let letters = ['a' .. 'z']<o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 9pt; FONT-FAMILY: 'Courier New'; mso-ansi-language: EN-GB"><SPAN style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp; </SPAN>let transp = letters |&gt; List.mapi (fun i l -&gt; l, List.nth letters ((i + 13) % 26))<SPAN style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp;&nbsp; </SPAN><o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 9pt; FONT-FAMILY: 'Courier New'; mso-ansi-language: EN-GB"><SPAN style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp; </SPAN>let rotchar c = List.assoc c transp<o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="FONT-SIZE: 9pt; FONT-FAMILY: 'Courier New'; mso-ansi-language: EN-GB"><SPAN style="mso-spacerun: yes">&nbsp;&nbsp;&nbsp; </SPAN>new string(s.ToCharArray() |&gt; Array.map rotchar)<o:p></o:p></SPAN></P>
<P class=MsoNormal style="MARGIN: 0cm 0cm 0pt"><SPAN lang=EN-GB style="mso-ansi-language: EN-GB"><o:p><FONT face="Times New Roman">&nbsp;</FONT></o:p></SPAN></P></FONT>