<html xmlns:v="urn:schemas-microsoft-com:vml" xmlns:o="urn:schemas-microsoft-com:office:office" xmlns:w="urn:schemas-microsoft-com:office:word" xmlns:m="http://schemas.microsoft.com/office/2004/12/omml" xmlns="http://www.w3.org/TR/REC-html40"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-16LE">

</head>

<body lang="EN-US" link="blue" vlink="purple" style="tab-interval:.5in">

<div class="WordSection1">

<h1><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
&quot;Times New Roman&quot;">Hacker's Guide to Q&amp;A Visualization<o:p></o:p></span></h1>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">Data Science and
visualization is about 90% data wrangling but that's no fun and, besides, we
only have 24 hours to build something great.<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">This guide is built to get
you to great because, let's face it, the judges won't be impressed by your
awesome ETL code no matter how important that is.<o:p></o:p></span></p>

<h2 id="Hacker&#39;sGuidetoQ&amp;AVisualization-Thisguidehas2parts(toolsanddata)butnotinthatorder"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">This
guide has 2 parts (tools and data) but not in that order&nbsp;<span style="mso-no-proof:yes"><!--[if gte vml 1]><v:shapetype id="_x0000_t75"
 coordsize="21600,21600" o:spt="75" o:preferrelative="t" path="m@4@5l@4@11@9@11@9@5xe"
 filled="f" stroked="f">
 <v:stroke joinstyle="miter"/>
 <v:formulas>
  <v:f eqn="if lineDrawn pixelLineWidth 0"/>
  <v:f eqn="sum @0 1 0"/>
  <v:f eqn="sum 0 0 @1"/>
  <v:f eqn="prod @2 1 2"/>
  <v:f eqn="prod @3 21600 pixelWidth"/>
  <v:f eqn="prod @3 21600 pixelHeight"/>
  <v:f eqn="sum @0 0 1"/>
  <v:f eqn="prod @6 1 2"/>
  <v:f eqn="prod @7 21600 pixelWidth"/>
  <v:f eqn="sum @8 21600 0"/>
  <v:f eqn="prod @7 21600 pixelHeight"/>
  <v:f eqn="sum @10 21600 0"/>
 </v:formulas>
 <v:path o:extrusionok="f" gradientshapeok="t" o:connecttype="rect"/>
 <o:lock v:ext="edit" aspectratio="t"/>
</v:shapetype><v:shape id="Picture_x0020_1" o:spid="_x0000_i1045" type="#_x0000_t75"
 alt="(wink)" style='width:12pt;height:12pt;visibility:visible;
 mso-wrap-style:square'>
 <v:imagedata src="Hacker's+Guide+to+Q&amp;A+Visualization_files/image001.png"
  o:title="(wink)"/>
</v:shape><![endif]--><!--[if !vml]--><img width="16" height="16" src="./hackers-guide_files/image001.png" alt="(wink)" v:shapes="Picture_x0020_1"><!--[endif]--></span><o:p></o:p></span></h2>

<div>

<div>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">The intention is to give you
sufficient understanding, some tools to get you started and to describe the
data you'll be working with.<br>
Remember that, except for the data section, it's just advice. Feel free to use
the tools you know and love and go as far off the rails as you need to...it
would not be hacking if you didn't.<o:p></o:p></span></p>

</div>

</div>

<h1 id="Hacker&#39;sGuidetoQ&amp;AVisualization-Data"><span style="font-family:
&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Data<o:p></o:p></span></h1>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">The data for this challenge
was extracted from a wickedly complicated database (<span class="SpellE">eGain</span>)
and lovingly, winnowed and massaged into the simple schema below:<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-no-proof:yes"><!--[if gte vml 1]><v:shape
 id="Picture_x0020_2" o:spid="_x0000_i1044" type="#_x0000_t75" style='width:351pt;
 height:3in;visibility:visible;mso-wrap-style:square'>
 <v:imagedata src="Hacker's+Guide+to+Q&amp;A+Visualization_files/image002.png"
  o:title="3d8a5271016e501abc68c94a653a4a6b"/>
</v:shape><![endif]--><!--[if !vml]--><img width="468" height="288" src="./hackers-guide_files/image003.png" v:shapes="Picture_x0020_2"><!--[endif]--></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><o:p></o:p></span></p>

<p><span class="GramE"><span style="font-family:&quot;Segoe UI&quot;,sans-serif">In order
to</span></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif"> ensure the
broadest participation possible (business users, data scientists and software
developers), I've published the data in three formats:<o:p></o:p></span></p>

<ol start="1" type="1">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
     mso-list:l8 level1 lfo1;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Multi-tabbed
     Excel File - If you are an expert with PowerPivot, Power BI, Tableau or
     other tools this format is very handy<br>
     <br>
     <a href="https://lexisai-hackathon.s3.amazonaws.com/med-malpractice-knowledge-graph/cardiovascular-medicine.xlsx">https://lexisai-hackathon.s3.amazonaws.com/med-malpractice-knowledge-graph/cardiovascular-medicine.xlsx</a><o:p></o:p></span></li>
 <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
     mso-list:l8 level1 lfo1;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">JSON or
     CSV - Work with ElasticSearch, <span class="SpellE">NoSql</span> or
     JavaScript visualization libraries, JSON is your friend.&nbsp; More of an <span class="SpellE">IPython</span>, Pandas or command line sort of gal, CSV is
     your ticket:<br>
     <br>
     <a href="https://lexisai-hackathon.s3.amazonaws.com/med-malpractice-knowledge-graph/cardiovascular-medicine-json.zip">https://lexisai-hackathon.s3.amazonaws.com/med-malpractice-knowledge-graph/cardiovascular-medicine-json.zip</a><br>
     <a href="https://lexisai-hackathon.s3.amazonaws.com/med-malpractice-knowledge-graph/cardiovascular-medicine-csv.zip">https://lexisai-hackathon.s3.amazonaws.com/med-malpractice-knowledge-graph/cardiovascular-medicine-csv.zip</a><o:p></o:p></span></li>
 <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
     mso-list:l8 level1 lfo1;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">SQLite -
     For my fellow full-stack development brothers and sisters, we have a <span class="SpellE">db</span> file that runs in the venerable and mighty
     in-memory RDBMs:<br>
     <br>
     <a href="https://lexisai-hackathon.s3.amazonaws.com/med-malpractice-knowledge-graph/cardiovascular-medicine.db">https://lexisai-hackathon.s3.amazonaws.com/med-malpractice-knowledge-graph/cardiovascular-medicine.db</a><o:p></o:p></span></li>
</ol>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">We'll touch on some of the
tools you can use to bend this data to your will in the sections below.<o:p></o:p></span></p>

<h2 id="Hacker&#39;sGuidetoQ&amp;AVisualization-What&#39;sinthesetablesanyway?"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">What's
in these tables anyway?<o:p></o:p></span></h2>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">First, it's important to
point out that the datasets <span class="GramE">contains</span> content for two
product areas:<o:p></o:p></span></p>

<ol start="1" type="1">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
     mso-list:l6 level1 lfo2;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Standard
     of Care Content (“SOC”)<o:p></o:p></span></li>
 <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
     mso-list:l6 level1 lfo2;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Case
     Value Assessment (“CVA”)<o:p></o:p></span></li>
</ol>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">Also, the dataset covers
cardiovascular medicine and is a focused subset of our entire corpus which
covers a huge range of medical practice areas.<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">Our business sponsors are
primarily interested in seeing what we can do with the SOC so that's what we'll
focus on here.<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">However, <span class="GramE">by
all means feel</span> free to build something spectacular with the CVA data as
well (it's a little more involved though).<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">Let's start with a simple <span class="SpellE">excercise</span> to map of the data to the UI so you get a better
feel of how things are connected.<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">Examples are in SQL but you
can slice and dice in Pandas or other favorite tool too (just examples).<o:p></o:p></span></p>

<h3 id="Hacker&#39;sGuidetoQ&amp;AVisualization-TheClustersTable:"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">The
Clusters Table:<o:p></o:p></span></h3>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">The clusters table is in the
middle of the diagram and referenced by most tables because it is the starting
point and glue for the Q&amp;A Knowledge Graph.<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">It defines medical subject
areas, starting points for Q&amp;A sections like the topics entry page:<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-no-proof:yes"><!--[if gte vml 1]><v:shape
 id="Picture_x0020_3" o:spid="_x0000_i1043" type="#_x0000_t75" style='width:351pt;
 height:258pt;visibility:visible;mso-wrap-style:square'>
 <v:imagedata src="Hacker's+Guide+to+Q&amp;A+Visualization_files/image004.png"
  o:title="81ee836a46a9b268c1f0c8342611d170"/>
</v:shape><![endif]--><!--[if !vml]--><img border="0" width="468" height="344" src="./hackers-guide_files/image005.png" v:shapes="Picture_x0020_3"><!--[endif]--></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">It has a parent/child <span class="SpellE">hierachy</span> and when you do a hierarchical query (or graph <span class="SpellE">vizualization</span>&nbsp;<span style="mso-no-proof:yes"><!--[if gte vml 1]><v:shape
 id="Picture_x0020_4" o:spid="_x0000_i1042" type="#_x0000_t75" alt="(smile)"
 style='width:12pt;height:12pt;visibility:visible;mso-wrap-style:square'>
 <v:imagedata src="Hacker's+Guide+to+Q&amp;A+Visualization_files/image006.png"
  o:title="(smile)"/>
</v:shape><![endif]--><!--[if !vml]--><img border="0" width="16" height="16" src="./hackers-guide_files/image006.png" alt="(smile)" v:shapes="Picture_x0020_4"><!--[endif]--></span>&nbsp;)&nbsp;you get something like
this:<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-no-proof:yes"><!--[if gte vml 1]><v:shape
 id="Picture_x0020_5" o:spid="_x0000_i1041" type="#_x0000_t75" style='width:351pt;
 height:401.25pt;visibility:visible;mso-wrap-style:square'>
 <v:imagedata src="Hacker's+Guide+to+Q&amp;A+Visualization_files/image007.png"
  o:title="3615ab88317ca30e2a03473a37f623e7"/>
</v:shape><![endif]--><!--[if !vml]--><img border="0" width="468" height="535" src="./hackers-guide_files/image008.png" v:shapes="Picture_x0020_5"><!--[endif]--></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">For SOC (<span class="SpellE">clusterId</span>
=&nbsp;<strong><span style="font-family:&quot;Segoe UI&quot;,sans-serif">1000018158</span></strong>)
in our dataset we get this:<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">"<strong><span style="font-family:&quot;Segoe UI&quot;,sans-serif">1000018158</span></strong>"
"SOC" "SOC" "C2"<br>
...<br>
"1000019343" "SOC -&gt; Hypertension"
"Hypertension" "C10"<br>
<strong><span style="font-family:&quot;Segoe UI&quot;,sans-serif;color:red">"1000019341"
"SOC -&gt; Myocardial Infarction" "Myocardial Infarction"
"C8"</span></strong><o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">And, as you can see, this is
the Breadcrumb Heading in the screenshot below.<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">&nbsp;<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-no-proof:yes"><!--[if gte vml 1]><v:shape
 id="Picture_x0020_6" o:spid="_x0000_i1040" type="#_x0000_t75" style='width:351pt;
 height:353.25pt;visibility:visible;mso-wrap-style:square'>
 <v:imagedata src="Hacker's+Guide+to+Q&amp;A+Visualization_files/image009.jpg"
  o:title="988eef9b1d6befa2c9a975e44f49eb69"/>
</v:shape><![endif]--><!--[if !vml]--><img border="0" width="468" height="471" src="./hackers-guide_files/image010.jpg" v:shapes="Picture_x0020_6"><!--[endif]--></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">This screenshot is a step in
the Standard of Care Questionnaire with the goal of finding "deviations in
the standard of care".<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">And shows a question,
possible answers/responses to those questions and "Why is this
important?" with useful guidance.<o:p></o:p></span></p>

<h3 id="Hacker&#39;sGuidetoQ&amp;AVisualization-TheQuestionsTable:"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">The
Questions Table:<o:p></o:p></span></h3>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">Ok, so what question should
I ask first?&nbsp; For SOC, it is very simple, questions are anchored by <span class="SpellE">ClusterId</span> (<span style="color:red">1000019341</span> for
Myocardial Infarction) and are asked in order.<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-no-proof:yes"><!--[if gte vml 1]><v:shape
 id="Picture_x0020_7" o:spid="_x0000_i1039" type="#_x0000_t75" style='width:351pt;
 height:99pt;visibility:visible;mso-wrap-style:square'>
 <v:imagedata src="Hacker's+Guide+to+Q&amp;A+Visualization_files/image011.png"
  o:title="295388953d9ca350ba3ef4d3c5189bf0"/>
</v:shape><![endif]--><!--[if !vml]--><img border="0" width="468" height="132" src="./hackers-guide_files/image012.png" v:shapes="Picture_x0020_7"><!--[endif]--></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><o:p></o:p></span></p>

<h3 id="Hacker&#39;sGuidetoQ&amp;AVisualization-TheAnswersTable:"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">The
Answers Table:<o:p></o:p></span></h3>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">Questions are tied to
answers in a few ways but for SOC you can simply join the questions table to
the answers table on <span class="SpellE">answerGroupId</span> and you are good
to go.<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-no-proof:yes"><!--[if gte vml 1]><v:shape
 id="Picture_x0020_8" o:spid="_x0000_i1038" type="#_x0000_t75" style='width:351pt;
 height:149.25pt;visibility:visible;mso-wrap-style:square'>
 <v:imagedata src="Hacker's+Guide+to+Q&amp;A+Visualization_files/image013.png"
  o:title="f1d329dc16f9d558dd5812b31cfa87bc"/>
</v:shape><![endif]--><!--[if !vml]--><img border="0" width="468" height="199" src="./hackers-guide_files/image014.png" v:shapes="Picture_x0020_8"><!--[endif]--></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><o:p></o:p></span></p>

<h3 id="Hacker&#39;sGuidetoQ&amp;AVisualization-The&quot;ClusterStartQuestions&quot;Table:"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">The
"Cluster Start Questions" Table:<o:p></o:p></span></h3>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">This structure is used to
bootstrap a Q&amp;A dialog.<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">When you select a Medical <span class="GramE">Topic</span> the application will want to know what sort of
analysis you want to do.&nbsp; In the case, a SOC or CVA analysis?<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">SOC is <span class="SpellE">straigtforward</span>,
you'll need this table only if you are working with CVA visualizations.<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-no-proof:yes"><!--[if gte vml 1]><v:shape
 id="Picture_x0020_9" o:spid="_x0000_i1037" type="#_x0000_t75" style='width:351pt;
 height:147pt;visibility:visible;mso-wrap-style:square'>
 <v:imagedata src="Hacker's+Guide+to+Q&amp;A+Visualization_files/image015.png"
  o:title="b81ddb3d942b2c1b41c5444dc73c7f48"/>
</v:shape><![endif]--><!--[if !vml]--><img border="0" width="468" height="196" src="./hackers-guide_files/image016.png" v:shapes="Picture_x0020_9"><!--[endif]--></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">SOC tables discussed at a
glance...<o:p></o:p></span></p>

<div>

<table class="MsoNormalTable" border="1" cellspacing="0" cellpadding="0" width="76%" style="width:76.46%;border-collapse:collapse;border:none;mso-border-alt:solid windowtext .75pt;
 mso-yfti-tbllook:1184">
 <colgroup><col style="width: 17.3675%;"><col style="width: 72.7937%;"></colgroup>
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes">
  <td style="border:solid windowtext 1.0pt;mso-border-alt:solid windowtext .75pt;
  padding:3.75pt 3.75pt 3.75pt 3.75pt">
  <p class="MsoNormal" align="center" style="text-align:center"><b><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Table
  Logical Name<o:p></o:p></span></b></p>
  </td>
  <td style="border:solid windowtext 1.0pt;border-left:none;mso-border-left-alt:
  solid windowtext .75pt;mso-border-alt:solid windowtext .75pt;padding:3.75pt 3.75pt 3.75pt 3.75pt">
  <p class="MsoNormal" align="center" style="text-align:center"><b><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Description<o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1;page-break-inside:avoid">
  <td style="border:solid windowtext 1.0pt;border-top:none;mso-border-top-alt:
  solid windowtext .75pt;mso-border-alt:solid windowtext .75pt;padding:3.75pt 3.75pt 3.75pt 3.75pt">
  <p class="MsoNormal"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
  &quot;Times New Roman&quot;">Clusters<o:p></o:p></span></p>
  </td>
  <td style="border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .75pt;
  mso-border-left-alt:solid windowtext .75pt;mso-border-alt:solid windowtext .75pt;
  padding:3.75pt 3.75pt 3.75pt 3.75pt">
  <p class="MsoNormal"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
  &quot;Times New Roman&quot;">Contains medical topics at their highest level. It is
  essentially the folder that houses the questions, answers, and
  annotations.&nbsp;<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2;page-break-inside:avoid">
  <td style="border:solid windowtext 1.0pt;border-top:none;mso-border-top-alt:
  solid windowtext .75pt;mso-border-alt:solid windowtext .75pt;padding:3.75pt 3.75pt 3.75pt 3.75pt">
  <p class="MsoNormal"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
  &quot;Times New Roman&quot;">Questions<o:p></o:p></span></p>
  </td>
  <td style="border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .75pt;
  mso-border-left-alt:solid windowtext .75pt;mso-border-alt:solid windowtext .75pt;
  padding:3.75pt 3.75pt 3.75pt 3.75pt">
  <p class="MsoNormal"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
  &quot;Times New Roman&quot;">Contains the Questions and the “Why is this important?”
  annotations and their hyperlink/<span class="SpellE">jcite</span> link to Lexis
  content.&nbsp;<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3;page-break-inside:avoid">
  <td style="border:solid windowtext 1.0pt;border-top:none;mso-border-top-alt:
  solid windowtext .75pt;mso-border-alt:solid windowtext .75pt;padding:3.75pt 3.75pt 3.75pt 3.75pt">
  <p class="MsoNormal"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
  &quot;Times New Roman&quot;">Answers<o:p></o:p></span></p>
  </td>
  <td style="border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .75pt;
  mso-border-left-alt:solid windowtext .75pt;mso-border-alt:solid windowtext .75pt;
  padding:3.75pt 3.75pt 3.75pt 3.75pt">
  <p class="MsoNormal"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
  &quot;Times New Roman&quot;">Contains <span class="GramE">all of</span> the possible
  answers users can select to the questions<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4;page-break-inside:avoid">
  <td style="border:solid windowtext 1.0pt;border-top:none;mso-border-top-alt:
  solid windowtext .75pt;mso-border-alt:solid windowtext .75pt;padding:3.75pt 3.75pt 3.75pt 3.75pt">
  <p class="MsoNormal"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
  &quot;Times New Roman&quot;">Case Answers<o:p></o:p></span></p>
  </td>
  <td style="border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .75pt;
  mso-border-left-alt:solid windowtext .75pt;mso-border-alt:solid windowtext .75pt;
  padding:3.75pt 3.75pt 3.75pt 3.75pt">
  <p class="MsoNormal"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
  &quot;Times New Roman&quot;">Contains the weighting that determines whether an answer
  will be a red light (Issue) or a green light (non-issue)<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5;mso-yfti-lastrow:yes;page-break-inside:avoid">
  <td style="border:solid windowtext 1.0pt;border-top:none;mso-border-top-alt:
  solid windowtext .75pt;mso-border-alt:solid windowtext .75pt;padding:3.75pt 3.75pt 3.75pt 3.75pt">
  <p class="MsoNormal"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
  &quot;Times New Roman&quot;">Cluster Start Questions<o:p></o:p></span></p>
  </td>
  <td style="border-top:none;border-left:none;border-bottom:solid windowtext 1.0pt;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid windowtext .75pt;
  mso-border-left-alt:solid windowtext .75pt;mso-border-alt:solid windowtext .75pt;
  padding:3.75pt 3.75pt 3.75pt 3.75pt">
  <p class="MsoNormal"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
  &quot;Times New Roman&quot;">Bootstraps a Q&amp;A flow for various types of analysis<o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

</div>

<h1 id="Hacker&#39;sGuidetoQ&amp;AVisualization-Tools"><span style="font-family:
&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Tools<o:p></o:p></span></h1>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">The tools in this section
are generally divided into these categories:<o:p></o:p></span></p>

<ol start="1" type="1">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
     mso-list:l5 level1 lfo3;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">General
     Purpose Workspaces - General purpose data analysis, data wrangling, etc.<o:p></o:p></span></li>
 <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
     mso-list:l5 level1 lfo3;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Graph
     Visualization Tools Graph Databases<o:p></o:p></span></li>
</ol>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">Note that some tools can do
"all of the above".<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">With a few exceptions, I've <span class="GramE">made an effort</span> to choose tools that:<o:p></o:p></span></p>

<ul type="disc">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
     mso-list:l3 level1 lfo4;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Are
     robust and work well<o:p></o:p></span></li>
 <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
     mso-list:l3 level1 lfo4;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Are
     multi-platform (Linux, Windows, MacOS)<o:p></o:p></span></li>
 <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
     mso-list:l3 level1 lfo4;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Are open
     source<o:p></o:p></span></li>
 <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
     mso-list:l3 level1 lfo4;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Represent
     the spectrum of modern data science and general programming languages<o:p></o:p></span></li>
</ul>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">I've also included some
tools and add-ins for business users and analysts to work with as well&nbsp;<span style="mso-no-proof:yes"><!--[if gte vml 1]><v:shape id="Picture_x0020_10"
 o:spid="_x0000_i1036" type="#_x0000_t75" alt="(smile)" style='width:12pt;
 height:12pt;visibility:visible;mso-wrap-style:square'>
 <v:imagedata src="Hacker's+Guide+to+Q&amp;A+Visualization_files/image006.png"
  o:title="(smile)"/>
</v:shape><![endif]--><!--[if !vml]--><img border="0" width="16" height="16" src="./hackers-guide_files/image006.png" alt="(smile)" v:shapes="Picture_x0020_10"><!--[endif]--></span><o:p></o:p></span></p>

<h3 id="Hacker&#39;sGuidetoQ&amp;AVisualization-Workspaces:"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Workspaces:<o:p></o:p></span></h3>

<ul type="disc">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
     mso-list:l2 level1 lfo5;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">SQLite
     Database Browser (SQL) - The queries in this guide were authored in the
     excellent SQLite Database Browser:&nbsp;&nbsp;<a href="http://sqlitebrowser.org/">http://sqlitebrowser.org/</a><o:p></o:p></span></li>
 <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
     mso-list:l2 level1 lfo5;tab-stops:list .5in"><span class="SpellE"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">JuPyter</span></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">
     (Python) - Notebooks are invaluable these days for analysis collaboration
     and rapid prototyping.&nbsp; One of the best is <span class="SpellE">JuPyter</span>:&nbsp;<a href="http://jupyter.org/">http://jupyter.org/</a><br>
     <br>
     Here's a <span class="GramE">1 minute</span> guide to get you going:<o:p></o:p></span></li>
 <ul type="circle">
  <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:
      auto;mso-list:l2 level2 lfo5;tab-stops:list 1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Download
      <span class="SpellE">Miniconda</span> and Install Python Distribution&nbsp;<a href="http://conda.pydata.org/miniconda.html">http://conda.pydata.org/miniconda.html<br>
      </a><a href="http://conda.pydata.org/miniconda.html"><br>
      </a><o:p></o:p></span></li>
  <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:
      auto;mso-list:l2 level2 lfo5;tab-stops:list 1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Install
      Core Dependencies<o:p></o:p></span></li>
 </ul>
</ul>

<pre style="margin-left:1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif">C:\&gt;conda install <span class="SpellE">numpy</span> pandas <span class="SpellE">scipy</span> <span class="SpellE">scikit</span>-learn <span class="SpellE">matplotlib</span> seaborn <span class="SpellE">jupyter</span> notebook<o:p></o:p></span></pre>

<p style="margin-left:1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif">&nbsp;<o:p></o:p></span></p>

<p style="margin-left:1.0in;text-indent:-.25in;mso-list:l2 level2 lfo5;
tab-stops:list 1.0in"><!--[if !supportLists]--><span style="font-size:10.0pt;
mso-bidi-font-size:12.0pt;font-family:&quot;Courier New&quot;;mso-fareast-font-family:
&quot;Courier New&quot;"><span style="mso-list:Ignore">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;
</span></span></span><!--[endif]--><span style="font-family:&quot;Segoe UI&quot;,sans-serif">Start
<span class="SpellE">Jupyter</span> - Your browser will open on&nbsp;<a href="http://localhost:8888/">http://localhost:8888<br>
</a><o:p></o:p></span></p>

<pre style="margin-left:1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif">c:\&gt;md c:\data-science<o:p></o:p></span></pre><pre style="margin-left:1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif">c:\&gt;cd c:\data-science<o:p></o:p></span></pre><pre style="margin-left:1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif">c:\data-science&gt;jupyter notebook<o:p></o:p></span></pre>

<p style="margin-left:1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif">&nbsp;<o:p></o:p></span></p>

<p style="margin-left:1.0in;text-indent:-.25in;mso-list:l2 level2 lfo5;
tab-stops:list 1.0in"><!--[if !supportLists]--><span style="font-size:10.0pt;
mso-bidi-font-size:12.0pt;font-family:&quot;Courier New&quot;;mso-fareast-font-family:
&quot;Courier New&quot;"><span style="mso-list:Ignore">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;
</span></span></span><!--[endif]--><span style="font-family:&quot;Segoe UI&quot;,sans-serif">Install
additional libraries (see below)<o:p></o:p></span></p>

<p style="margin-left:1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif">&nbsp;<o:p></o:p></span></p>

<ul type="disc">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
     mso-list:l2 level1 lfo5;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">plot.ly
     (Python) - Don't have time to install tools?&nbsp; Want a quick
     one-stop-shop studio to work in?&nbsp; Use plot.ly:&nbsp;&nbsp;<a href="https://plot.ly/">https://plot.ly</a><o:p></o:p></span></li>
 <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
     mso-list:l2 level1 lfo5;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Microsoft
     Excel (WYSWIG) - Excel has come a long way and new <span class="SpellE">addins</span>
     have extended <span class="SpellE"><span class="GramE">it's</span></span>
     capabilities as a serious data science tool.<br>
     <br>
     Enable the following add-ins and install these tools to get you going:<o:p></o:p></span></li>
 <ul type="circle">
  <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:
      auto;mso-list:l2 level2 lfo5;tab-stops:list 1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Power
      BI -&nbsp;<a href="https://powerbi.microsoft.com/en-us/downloads/">https://powerbi.microsoft.com/en-us/downloads/</a><o:p></o:p></span></li>
  <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:
      auto;mso-list:l2 level2 lfo5;tab-stops:list 1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">GIGRAPH
      Network <span class="SpellE">Vizualization</span> -&nbsp;<a href="https://appsource.microsoft.com/en-us/product/office/WA104379873?tab=Overview">https://appsource.microsoft.com/en-us/product/office/WA104379873?tab=Overview</a><o:p></o:p></span></li>
  <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:
      auto;mso-list:l2 level2 lfo5;tab-stops:list 1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Also,
      check out the endless add-ins available for Power BI and Excel:&nbsp;<a href="https://appsource.microsoft.com/en-us/marketplace/apps?search=&amp;page=1&amp;product=power-bi-visuals&amp;category=analytics%3Bartifical-intelligence&amp;src=office">https://appsource.microsoft.com/en-us/marketplace/apps?search=&amp;page=1&amp;product=power-bi-visuals&amp;category=analytics%3Bartifical-intelligence&amp;src=office</a><br>
      </span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
      &quot;Times New Roman&quot;;mso-no-proof:yes"><img border="0" width="512" height="384" id="_x0000_i1035" src="./hackers-guide_files/gigraphstore1.png" alt="Image result for excel GIGRAPH"></span><span style="font-family:
      &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;"><o:p></o:p></span></li>
 </ul>
</ul>

<h3 id="Hacker&#39;sGuidetoQ&amp;AVisualization-GraphVisualization:"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Graph
Visualization:<o:p></o:p></span></h3>

<ul type="disc">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
     mso-list:l0 level1 lfo6;tab-stops:list .5in"><span class="SpellE"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Gephi</span></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">
     (WYSIWG) - It's not for everyone, has learning curve (no difficult, just
     lots of options) but <span class="SpellE">Gephi</span> is an amazing
     all-in-one Graph <span class="SpellE">Vizualization</span>
     platform:&nbsp;&nbsp;<a href="https://gephi.org/">https://gephi.org/</a><br>
     <br>
     </span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
     &quot;Times New Roman&quot;;mso-no-proof:yes"><img border="0" width="580" height="358" id="_x0000_i1034" src="./hackers-guide_files/home_screenshot.jpg" alt="Image result for Gephi"></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;
     mso-fareast-font-family:&quot;Times New Roman&quot;"><o:p></o:p></span></li>
</ul>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">&nbsp;<o:p></o:p></span></p>

<ul type="disc">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
     mso-list:l7 level1 lfo7;tab-stops:list .5in"><span class="SpellE"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">NetworkX</span></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">
     (Python) - Much more than a <span class="SpellE">vizualization</span> library
     (has algorithms too).&nbsp; Among one of the best for Python:&nbsp; <a href="https://networkx.github.io/">https://networkx.github.io/</a><br>
     <br>
     </span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-no-proof:yes"><!--[if gte vml 1]><v:shape
      id="Picture_x0020_22" o:spid="_x0000_i1033" type="#_x0000_t75" style='width:468pt;
      height:249pt;visibility:visible;mso-wrap-style:square'>
      <v:imagedata src="Hacker's+Guide+to+Q&amp;A+Visualization_files/image017.png"
       o:title=""/>
     </v:shape><![endif]--><!--[if !vml]--><img border="0" width="624" height="332" src="./hackers-guide_files/image018.jpg" v:shapes="Picture_x0020_22"><!--[endif]--></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;"><o:p></o:p></span></li>
</ul>

<p class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
margin-left:.5in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
&quot;Times New Roman&quot;"><o:p>&nbsp;</o:p></span></p>

<ul type="disc">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
     mso-list:l7 level1 lfo7;tab-stops:list .5in"><span class="SpellE"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Cytoscape</span></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">
     (WYSIWG and JavaScript) - Amazing...it is both a standalone analysis
     environment and JavaScript library<o:p></o:p></span></li>
 <ul type="circle">
  <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:
      auto;mso-list:l7 level2 lfo7;tab-stops:list 1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">JavaScript:&nbsp;<a href="http://js.cytoscape.org/">http://js.cytoscape.org/</a><o:p></o:p></span></li>
  <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
      mso-list:l7 level2 lfo7;tab-stops:list 1.0in"><span class="SpellE"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Standalone:<a href="http://www.cytoscape.org/">http://www.cytoscape.org/</a></span></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;"><o:p></o:p></span></li>
 </ul>
</ul>

<p class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
margin-left:.5in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
&quot;Times New Roman&quot;;mso-no-proof:yes"><img border="0" width="735" height="441" id="_x0000_i1032" src="./hackers-guide_files/DisGeNET.png" alt="Image result for cytoscape"></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;"><o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-no-proof:yes"><img border="0" width="694" height="416" id="_x0000_i1031" src="./hackers-guide_files/d3_2.jpg" alt="Image result for cytoscape.js"></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">&nbsp;<o:p></o:p></span></p>

<ul type="disc">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
     mso-list:l1 level1 lfo8;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">sigma.js
     (JavaScript) - The secret sauce behind many visualization libraries.&nbsp;
     <span class="SpellE">Beutiful</span> graphs without a Ph. D. in
     3d.js:&nbsp;&nbsp;<a href="http://sigmajs.org/">http://sigmajs.org/</a><br>
     <br>
     </span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
     &quot;Times New Roman&quot;;mso-no-proof:yes"><img border="0" width="800" height="426" id="_x0000_i1030" src="./hackers-guide_files/cambridge-intelligence-time-bar.png" alt="Image result for sigma.js"></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;
     mso-fareast-font-family:&quot;Times New Roman&quot;"><o:p></o:p></span></li>
</ul>

<h3 id="Hacker&#39;sGuidetoQ&amp;AVisualization-GraphDatabases:"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Graph
Databases:<o:p></o:p></span></h3>

<ul type="disc">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
     mso-list:l9 level1 lfo9;tab-stops:list .5in"><span class="SpellE"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">TinkerPop</span></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">
     (multiple) - The single most important Graph "stack" to
     date.&nbsp; It's an API and a <span class="SpellE">dtabase</span> and has
     hooks for almost any graph and non-graph database that matter's.&nbsp;
     Lean this API and you have access to a <span class="SpellE">vitually</span>
     unlimited ecosystem of graph analytics tool:<br>
     <br>
     <a href="https://academy.datastax.com/resources/getting-started-tinkerpop-and-gremlin">https://academy.datastax.com/resources/getting-started-tinkerpop-and-gremlin</a><br>
     <a href="http://tinkerpop.apache.org/docs/3.1.0-incubating/tutorials-getting-started.html">http://tinkerpop.apache.org</a><o:p></o:p></span></li>
 <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
     mso-list:l9 level1 lfo9;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Gremlin
     Servers - <span class="SpellE">TinkerPop's</span> Gremlin has lightweight,
     standalone server that work out of the box:&nbsp;&nbsp;<o:p></o:p></span></li>
 <ul type="circle">
  <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:
      auto;mso-list:l9 level2 lfo9;tab-stops:list 1.0in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">Gremlin
      Server -&nbsp;<a href="http://tinkerpop.apache.org/docs/current/reference/#gremlin-server">http://tinkerpop.apache.org/docs/current/reference/#gremlin-server</a><o:p></o:p></span></li>
  <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:
      auto;mso-list:l9 level2 lfo9;tab-stops:list 1.0in"><span class="SpellE"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">TinkerGraph</span></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">
      -&nbsp;<a href="http://tinkerpop.apache.org/docs/current/reference/#tinkergraph-gremlin">http://tinkerpop.apache.org/docs/current/reference/#tinkergraph-gremlin</a><o:p></o:p></span></li>
 </ul>
</ul>

<p style="margin-left:.25in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><a href="http://tinkerpop.apache.org/docs/current/reference/#gremlin-server"><br>
</a></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-no-proof:yes"><img border="0" width="587" height="203" id="_x0000_i1029" src="./hackers-guide_files/gremlin-server-protocol.png" alt="https://academy.datastax.com/sites/default/files/gremlin-server-protocol.png"></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><br>
<a href="http://tinkerpop.apache.org/docs/current/reference/#gremlin-server"><br>
</a><o:p></o:p></span></p>

<ul type="disc">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;margin-bottom:12.0pt;
     mso-list:l4 level1 lfo10;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">neo4j -
     Neo4j is a commercial product but the community edition is useful for
     prototyping and it is an all in one database, visualization and wrangling
     setup:&nbsp; &nbsp;<a href="https://neo4j.com/download/">https://neo4j.com/download/</a><br>
     <br>
     You'll have to learn the Cypher Query language but it's not that hard to
     pick up:&nbsp;&nbsp;<a href="https://neo4j.com/developer/cypher-query-language/">https://neo4j.com/developer/cypher-query-language/</a><br>
     <br>
     Some inspiration:&nbsp;<a href="https://offshoreleaks.icij.org/#_ga=2.228660124.1057063318.1507812556-1860127475.1507812556">https://offshoreleaks.icij.org/#_ga=2.228660124.1057063318.1507812556-1860127475.1507812556</a><br>
     <br>
     </span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
     &quot;Times New Roman&quot;;mso-no-proof:yes"><img border="0" width="535" height="402" id="_x0000_i1028" src="./hackers-guide_files/using-neo4j-for-enterprise-metadata-requirements-17-638.jpg" alt="https://image.slidesharecdn.com/usingneo4jforenterprisemetadatarequirements-160613091446/95/using-neo4j-for-enterprise-metadata-requirements-17-638.jpg?cb=1465809382"></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;"><o:p></o:p></span></li>
 <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
     mso-list:l4 level1 lfo10;tab-stops:list .5in"><span style="font-family:
     &quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">ElasticSearch
     / Kibana / X-Pack - <span class="SpellE">ElasticsSearch</span> and Kibana
     are open source, X-Pack is not (for production use).&nbsp; Nevertheless,
     it is an extremely powerful and scalable solution:<o:p></o:p></span></li>
</ul>

<p style="margin-left:.5in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><a href="https://www.elastic.co/guide/en/kibana/5.6/xpack-graph.html">https://www.elastic.co/guide/en/kibana/5.6/xpack-graph.html</a><o:p></o:p></span></p>

<p style="margin-left:.5in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><a href="https://www.elastic.co/downloads">https://www.elastic.co/downloads</a><o:p></o:p></span></p>

<p style="margin-left:.5in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><a href="https://www.elastic.co/downloads/x-pack">https://www.elastic.co/downloads/x-pack</a><o:p></o:p></span></p>

<p style="margin-left:.5in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;
mso-no-proof:yes"><img border="0" width="614" height="360" id="_x0000_i1027" src="./hackers-guide_files/kibana-graph.jpg" alt="Image result for elasticsearch graph"></span><span style="font-family:
&quot;Segoe UI&quot;,sans-serif"><o:p></o:p></span></p>

<p style="margin-left:.5in;text-indent:-.25in;mso-list:l4 level1 lfo10;
tab-stops:list .5in"><!--[if !supportLists]--><span style="font-size:10.0pt;
mso-bidi-font-size:12.0pt;font-family:Symbol;mso-fareast-font-family:Symbol;
mso-bidi-font-family:Symbol"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></span></span><!--[endif]--><span class="SpellE"><span style="font-family:
&quot;Segoe UI&quot;,sans-serif">JanusGraph</span></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif">
- Titan DB is dead, long live <span class="SpellE">JanusGraph</span>:&nbsp;&nbsp;<a href="http://janusgraph.org/">http://janusgraph.org/</a>&nbsp;(Warning:
industrial strength and a bit of a learning curve but worth it...true OSS, full
text search, structured queries, graph queries...incredible)<o:p></o:p></span></p>

<p style="margin-left:.5in"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;
mso-no-proof:yes"><img border="0" width="43" height="14" id="_x0000_i1026" src="./hackers-guide_files/janusgraph.png" alt="Image result for janusgraph"></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif"><o:p></o:p></span></p>

<ul type="disc">
 <li class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
     mso-list:l4 level1 lfo10;tab-stops:list .5in"><span class="SpellE"><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">ArangoDB</span></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;">
     - Another <span class="GramE">powerful</span> Graph DB&nbsp;<a href="https://www.arangodb.com/">https://www.arangodb.com/</a><br>
     <br>
     </span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;mso-fareast-font-family:
     &quot;Times New Roman&quot;;mso-no-proof:yes"><img border="0" width="627" height="376" id="_x0000_i1025" src="./hackers-guide_files/graph4.png" alt="Image result for ArangoDB"></span><span style="font-family:&quot;Segoe UI&quot;,sans-serif;
     mso-fareast-font-family:&quot;Times New Roman&quot;"><o:p></o:p></span></li>
</ul>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">&nbsp;<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">&nbsp;<o:p></o:p></span></p>

<p><span style="font-family:&quot;Segoe UI&quot;,sans-serif">&nbsp;<o:p></o:p></span></p>

</div>




</body></html>
