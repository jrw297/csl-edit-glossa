# csl-edit-glossa

This is an attempt to edit a citation style so that no Middle Initial is noted in the long name form of bibliographic citations

This XML file does not appear to have any style information associated with it. The document tree is shown below.
<style xmlns="http://purl.org/net/xbiblio/csl" class="in-text" version="1.0" initialize-with-hyphen="false" demote-non-dropping-particle="sort-only" default-locale="en-GB">
<script id="eppiocemhmnlbhjplcgkofciiegomcon"/>
<script/>
<script/>
<info>
<title>Journal of Historical Linguistics - Jeffrey Wall</title>
<title-short>JHL</title-short>
<id>http://csl.mendeley.com/styles/28042991/journal-of-historical-linguistics</id>
<link href="http://www.zotero.org/styles/journal-of-historical-linguistics" rel="self"/>
<link href="http://www.zotero.org/styles/zoological-journal-of-the-linnean-society" rel="template"/>
<link href="https://benjamins.com/#catalog/journals/jhl/submission" rel="documentation"/>
<link href="https://www.benjamins.com/series/jhl/jhl_stylesheet.pdf" rel="documentation"/>
<author>
<name>Patrick O'Brien</name>
<email>obrienpat86@gmail.com</email>
</author>
<contributor>
<name>Jeffrey Wall</name>
<uri/>
</contributor>
<category citation-format="author-date"/>
<category field="linguistics"/>
<issn>2210-2116</issn>
<eissn>2210-2124</eissn>
<updated>2025-03-12T09:36:21+00:00</updated>
<rights license="http://creativecommons.org/licenses/by-sa/3.0/">This work is licensed under a Creative Commons Attribution-ShareAlike 3.0 License</rights>
</info>
<locale xml:lang="en">
<terms>
<term name="by">ed. by</term>
</terms>
</locale>
<macro name="editor-translator">
<names variable="editor translator" prefix="(" suffix=")" delimiter=", ">
<name and="text" initialize-with="" delimiter=", "/>
<et-al font-style="italic"/>
<label form="short" prefix=", " text-case="capitalize-first"/>
</names>
</macro>
<macro name="author">
<names variable="author">
<name delimiter-precedes-last="contextual" initialize="false" initialize-with="." name-as-sort-order="first" and="symbol"/>
<et-al font-style="italic"/>
<label form="short" prefix=" (" suffix=")" text-case="capitalize-first"/>
<substitute>
<names variable="editor"/>
<names variable="translator"/>
<text macro="title"/>
</substitute>
</names>
</macro>
<macro name="author-short">
<names variable="author">
<name form="short"/>
<et-al font-style="italic"/>
<substitute>
<names variable="editor"/>
<names variable="translator"/>
<choose>
<if type="bill book graphic legal_case legislation motion_picture report song" match="any">
<text variable="title" form="short" font-style="italic"/>
</if>
<else>
<text variable="title" form="short" quotes="true"/>
</else>
</choose>
</substitute>
</names>
</macro>
<macro name="title">
<choose>
<if type="bill book graphic legal_case legislation motion_picture report song" match="any">
<text variable="title" font-style="italic"/>
</if>
<else>
<text variable="title"/>
</else>
</choose>
</macro>
<macro name="publisher">
<group delimiter=": ">
<text variable="publisher-place"/>
<text variable="publisher"/>
</group>
</macro>
<citation collapse="year-suffix" and="symbol" et-al-min="4" et-al-use-first="1" et-al-subsequent-min="3" et-al-subsequent-use-first="1" disambiguate-add-year-suffix="true" year-suffix-delimiter=",">
<sort>
<key variable="issued"/>
<key variable="author"/>
</sort>
<layout delimiter=", " prefix="(" suffix=")">
<group>
<text macro="author-short" text-case="capitalize-first" suffix=" "/>
<date variable="issued">
<date-part name="year"/>
</date>
<group prefix=": ">
<text variable="locator" prefix=" "/>
</group>
</group>
</layout>
</citation>
<bibliography hanging-indent="false">
<sort>
<key macro="author-short"/>
<key variable="issued"/>
</sort>
<layout suffix=".">
<text macro="author" text-case="capitalize-first" suffix="."/>
<date variable="issued" text-case="uppercase" prefix=" " suffix=".">
<date-part name="year"/>
</date>
<choose>
<if type="bill book graphic legal_case legislation motion_picture report song" match="any">
<group suffix=".">
<text macro="title" prefix=" "/>
<text macro="editor-translator" prefix=" "/>
</group>
<text prefix=" " suffix="." macro="publisher"/>
</if>
<else-if type="chapter paper-conference" match="any">
<text macro="title" prefix=" " suffix="."/>
<group prefix=".">
<group delimiter=" " prefix=" ">
<text variable="container-title" font-style="italic"/>
<group suffix=".">
<text term="by" suffix=" "/>
<names variable="editor translator" delimiter="," suffix=",">
<name delimiter=" " and="symbol" delimiter-precedes-last="never" initialize="false" name-as-sort-order="first" sort-separator=" "/>
</names>
<text variable="page" prefix=" " suffix="."/>
</group>
<text macro="publisher"/>
</group>
</group>
</else-if>
<else-if type="thesis" match="any">
<group suffix=".">
<text macro="title" prefix=" "/>
<text macro="editor-translator" prefix=" "/>
</group>
<text prefix=" Unpublished thesis, " suffix="." variable="publisher"/>
</else-if>
<else>
<group suffix=".">
<text macro="title" prefix=" "/>
<text macro="editor-translator" prefix=" "/>
</group>
<group prefix=" " suffix=".">
<text variable="container-title" font-style="italic"/>
<group delimiter=":" prefix=" " suffix=".">
<text variable="volume"/>
<text variable="issue"/>
</group>
<text variable="page"/>
</group>
</else>
</choose>
</layout>
</bibliography>
</style>
