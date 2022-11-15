https://github.com/dotnet/maui/issues/11302


### Description

When an SVG graphic contains more complicated text elements the conversion into an PNG is not correct. The following is an example of and SVG <text/> element that .Net MAUI renders into a PNG file incorrectly...

<text
   class="st11 st12"
   id="text91"
   x="37.237553"
   y="85.818047"><tspan
   style="fill:#ff0000"
   id="tspan1155">Hello</tspan>World</text><text
   class="st11 st12"
   id="text91-7"
   x="54.880131"
   y="111.79536"
   style="font-size:24px;font-family:TimesNewRomanPS-BoldMT">This is <tspan
   style="font-size:24px;fill:#ff0000"
   id="tspan1155-1">Not </tspan>Correct</text><text
   class="st11 st12"
   id="text91-7-2"
   x="165.71021"
   y="180.68277"
   style="font-size:24px;font-family:TimesNewRomanPS-BoldMT;text-align:center;text-anchor:middle"><tspan
     sodipodi:role="line"
     id="tspan5734"
     x="165.71021"
     y="180.68277">Line 1 - No Spaces</tspan><tspan
     sodipodi:role="line"
     id="tspan5736"
     x="165.71021"
     y="210.68277">Line 2 - Spaces</tspan></text>

### Steps to Reproduce

1. Create a new .Net MAUI Android project using the standard "Hello World" template.
2. Create a new SVG graphic that contains a complex text - for example a single text element with multiple colors.
3. Include the SVG in the project as appropriate.
4. Compile and execute the application.
5. Note that the results are incorrect.

Sample project referenced in public repo.



### Link to public reproduction project repository

https://github.com/vr4guid/MauiDefect-SVG-1

### Version with bug

6.0.486 (current)

### Last version that worked well

Unknown/Other

### Affected platforms

Android

### Affected platform versions

Android 12.0, Android 13.0

### Did you find any workaround?

At present the only known workaround is to create PNG graphics outside of the .Net MAUI toolchain - which is counter to a core objective of .Net MAUI.

### Relevant log output

_No response_
