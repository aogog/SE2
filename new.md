# Order  
> ## 1. Headings 
> ## 2. Paragraphs
> ## 3. Line Breaks  
> ## 4. Bold  
> ## 5. Italic  
> ## 6. Bold & Italic  
> ## 7. Blockquotes  
> ## 8. Ordered Lists  
> ## 9. Unordered Lists  
> ## 10. Adding Element in Lists  
> ## 11. Code  
> ## 12. Escaping Backticks  
> ## 13. Code Blocks  
> ## 14. Horizontal Rules  
> ## 15. Links  
> ## 16. URLs and Email Addresses  
> ## 17. Formatting Links  
> ## 18. Reference-style Links  
> ## 19. Images  
> ## 20. Linking Images  
> ## 21. Escaping Characters  
> ## 22. Characters You can Escape  
> ## 23. HTML  
# 1. Headings  
To create a headings, add number signs(#) in front a word or pahse.
- ## `The number of # is size!`  
### Ex)  
```
# Heading level 1
## Heading level 2
### Heading level 3
#### Heading level 4
##### Heading level 5
###### Heading level 6
```  
### Result :  
# Heading level 1  
## Heading level 2  
### Heading level 3  
#### Heading level 4  
##### Heading level 5  
###### Heading level 6  
***
- ## `Alternative Using ' == ' or ' -- '`  
### Ex)  
```
Heading level 1        
===============
```
### Result :  
&nbsp;Heading level 1
===============  

### Ex)  
```  
Heading level 2        
---------------
```  

### Result :  
&nbsp;Heading level 2
---------------  

* * *
# 2. Paragraphs  
To create paragraphs, use a blank line to separte one or more lines of text.  
### Ex)  
```
I like computer  

I like game  
```  
### Result :  
&nbsp;I line computer.  

&nbsp;I like game.  

* * *
# 3. Line Breaks  
To create a line break, end a line with **two or more spaces**, and then type return.  
### Ex)  
```
This is the first line.  
And this is the second line.
```  
### Result :  
&nbsp;This is the first line.  
&nbsp;This is the second line.

* * *
# 4. Bold  
To bold text, add two asterisks(\*) or underscores(\_) before and after a word or phase.
```
This text is **really** important.  
This text is __really__ important.  
```
### Result :    
&nbsp;This text is **really** important.  
&nbsp;This text is __really__ important.  

* * *
# 5. Italic
To italicize text, add one asterisks(\*) or underscores(\_) before and after a word or phase.
### Ex)  
```
This is a *test* line.   
This is a _test_ line.   
```  
### Result :  
&nbsp;This is a *test* line.  
&nbsp;This is a _test_ line.  
* * *
# 6. Bold & Italic  
To emphasize text with bold and italics at the same time, add three asterisks(\*) or underscores(\_) before and after a word or phrase.  
### Ex)  
```
This is a ***test line***.
```  

### Result :  
&nbsp;This is a ***test line***.  

* * *
# 7. Blockquotes  
To create a blockquote, add a > in front of a paragraph  
### Ex)  
```
> This is a test line.
```  

### Result :  
> This is a test line.  

### `Blockquotes with Multiple Paragraphs.`  
`-` Blockquotes can contain multiple paragraphs. Add a > on the blank lines between the paragraphs.  
### Ex)  
```
> This is a test line.  
>  
> This is a Test line.  
```  

### Result :  
> This is a test line.  
>  
> This is a Test line.  

### `Nested Blockquotes`  
`-` Blockquotes can be nested. Add a >> in front of the paragraph you want to nest. 
### Ex)  
``` 
> This is a test line.  
>
>> This is a Test line.  
```
### Result :  
> This is a test line.  
>  
>> This is a Test line.  

### `Blockquotes with Other Elements.`  
`-` Blockquotes can contain other Markdown formatted elements. Not all elements can be used — you’ll need to experiment to see which ones work.  
### Ex)  
```
> ## This is a test line.  
>
> - This is a test line.  
>  
> *This* is a test line.  
```
### Result :  
> ## This is a test line.  
> 
> - This is a test line.  
>  
> *This* is a test line.  

***  

# 8. Ordered Lists  
To create an ordered list, add line items with numbers followed by periods. **The numbers don’t have to be in numerical order, but the list should start with the number one**.  
### Ex)  
```
1. First  
3. Second  
9. Third  
```
### Result :  
1. First  
3. Second  
9. Third  

* * *
# 9. Unordered Lists  
To create an unordered list, add dashes (-), asterisks (*), or plus signs (+) in front of line items. Indent one or more items to create a nested list.  
### Ex)  
```  
- First  
* Second  
+ Third  
  - Fourth
  ```     
### Result :  
  - First  
  * Second  
  + Third  
    - Fourth 

	* * *
# 10. Adding Element in Lists  
	To add another element in a list while preserving the continuity of the list, indent the element four spaces or one tab, as shown in the following examples.  

## 1. Paragraphs  
### Ex)  
	```
	*   This is the first line.
	*   This is the Second line.

	    I need to add another paragraph below the second line.

		*   This is the Third line.  
		```  
### Result :  
		 * This is the First line.  
		  * This is the Second line. 

		      I need to add another paragraph below the second line.  
			  * This is the Third line.  
			   

## 2. Blockquotes  
### Ex)  
			  ```
			  *   This is the first list item.
			  *   Here's the second list item.

			      > A blockquote would look great below the second list item.

				  *   And here's the third list item.
				  ```  
### Result :  
				  *   This is the first list item.
				  *   Here's the second list item.

				      > A blockquote would look great below the second list item.

					  *   And here's the third list item.  

## 3. Code Blocks  
					        Code blocks are normally indented four spaces or one tab. When they’re in a list, indent them eight spaces or two tabs.  
### Ex)  
							```
							1.  Open the file.
							2.  Find the following code block on line 21:

							        <html>
									          <head>
											              <title>Test</title>
														            </head>

																	3.  Update the title to match the name of your website.
																	```  
### Result :  
																	1.  Open the file containing the Linux mascot.
																	2.  Marvel at its beauty.

																	    ![Tux, the Linux mascot](./image/tux.png)

		3.  Close the file.  

## 4. Lists  
		You can nest an unordered list in an ordered list, or vice versa.  
### Ex)  
		```
		1. First item
		2. Second item
		3. Third item
		    - Indented item
			    - Indented item
				4. Fourth item
				```  

### Result :  
				1. First item
				2. Second item
				3. Third item
				    - Indented item
					    - Indented item
						4. Fourth item  

						***

# 11. Code  
						To denote a word or phrase as code, enclose it in backticks (`).  
### Ex)  
						```
						At the command prompt, type `nano`.
						```  

### Result :  
						At the command prompt, type `nano`.  
						***  
#  
# 12. Escaping Backticks  
						If the word or phrase you want to denote as code includes one or more backticks, you can escape it by enclosing the word or phrase in double backticks (``).  
### Ex)  
						```
						``Use `code` in your Markdown file.``
						```  

### Result :  
						``Use `code` in your Markdown file.``  
						***  
#  
# 13. Code Blocks  
						To create code blocks, indent every line of the block by at least four spaces or one tab.  
### Ex)  
						```
						    <html>
							      <head>
								        </head>
										    </html>
											```  

### Result :  
											    <html>
												      <head>
													        </head>
															    </html>  
																***
#  
# 14. Horizontal Rules  
																To create a horizontal rule, use three or more asterisks (***), dashes (---), or underscores (___) on a line by themselves.  
### Ex)   
																```
																For compatibility, put blank lines before and after horizontal rules.

																***

																---

																_________________
																```  

### Result :  
																***

																---

																_________________  

																***
#

# 15. Links  
																To create a link, enclose the link text in brackets (e.g., [Duck Duck Go]) and then follow it immediately with the URL in parentheses (e.g., (https://duckduckgo.com)).  
### Ex)  
																```
																My favorite search engine is [Duck Duck Go](https://duckduckgo.com).
																```  

### Result :  
																My favorite search engine is [Duck Duck Go](https://duckduckgo.com).  
																  - ### `Adding Titles`
																      You can optionally add a title for a link. This will appear as a tooltip when the user hovers over the link. To add a title, enclose it in parentheses after the URL.  
																	      ### Ex)  
																	      ```
																		      My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").
																			      ```

																				      ### Result :  
																				      My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").  

																					  ***

## 16. URLs and Email Addresses  
																					  To quickly turn a URL or email address into a link, enclose it in angle brackets.  
### Ex)   
																					  ```
																					  <https://www.markdownguide.org>
																					  <fake@example.com>
																					  ```  

### Result :  
																					  <https://www.markdownguide.org>  
																					  <fake@example.com>  

																					  ***
## 17. Formatting Links  
To emphasize links, add asterisks before and after the brackets and parentheses. To denote links as code, add backticks in the brackets.  
### Ex)  
```
I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code).
```  

### Result :  
I love supporting the **[EFF](https://eff.org)**.  
This is the *[Markdown Guide](https://www.markdownguide.org)*.  
See the section on [`code`](#code).  
***  

## 18. Reference-style Links  
Reference-style links are a special kind of link that make URLs easier to display and read in Markdown. Reference-style links are constructed in two parts: the part you keep inline with your text and the part you store somewhere else in the file to keep the text easy to read.  
  - ### Formatting the First Part of the Link  
      The first part of a reference-style link is formatted with two sets of brackets. The first set of brackets surrounds the text that should appear linked. The second set of brackets displays a label used to point to the link you’re storing elsewhere in your document.  
	      Although not required, you can include a space between the first and second set of brackets. The label in the second set of brackets is not case sensitive and can include letters, numbers, spaces, or punctuation.  
		      This means the following example formats are roughly equivalent for the first part of the link:  
			   ``` 
			   [Example][Link]  
			   ```
			     - ### Formatting the Second Part of the Link  
				     The second part of a reference-style link is formatted with the following attributes:  
					     1. The label, in brackets, followed immediately by a colon and at least one space (e.g., [label]: ).  
						     2. The URL for the link, which you can optionally enclose in angle brackets.  
							     3. The optional title for the link, which you can enclose in double quotes, single quotes, or parentheses.  
								   This means the following example formats are all roughly equivalent for the second part of the link:  
								   ```
								   [Link]: https://Exmaple.com "Hello"
								   ```  
### Result :  

								   [Example][Link]  

								   [Link]: htts=//Example.com "Hello"  

								   ***  

## 19. Images  
								   To add an image, add an exclamation mark (!), followed by alt text in brackets, and the path or URL to the image asset in parentheses. You can optionally add a title after the URL in the parentheses.  
### Ex)  
								   ```
								   ![Penguin is Cute!](./image/tux.png "TUX")
								   ```  

### Result :  
								   ![Penguin is Cute!](./image/tux.png  "TUX")  
								   ***  

## 20. Linking Images  
								   To add a link to an image, enclose the Markdown for the image in brackets, and then add the link in parentheses.  
### Ex)  
								   ```
								   [![Penguin!](./image/tux.png "Penguin!")](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv) 
								   ```
### Result :  
								   [![Penguin!](./image/tux.png "Penguin!")](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)  
								   ***  

## 21. Escaping Characters  
								   To display a literal character that would otherwise be used to format text in a Markdown document, add a backslash (\) in front of the character.  
### Ex)  
								   ```
								   \* Without the backslash, this would be a bullet in an unordered list.
								   ```  
### Result :  
								   \* Without the backslash, this would be a bullet in an unordered list.  
								   ***  

## 22. Characters You can Escape  
								     1. \\   : backslash  
									   2. \`   : backtick  
									     3. \*   : asterisk  
										   4. \_   : underscore  
										     5. \{ } : curly braces  
											   6. \[ ] : brackets  
											     7. \< > : angle brackets  
												   8. \( ) : parentheses  
															   9. \#   : pound sign  
																	    10. \+  : plus sign  
																			  11. \-  : mius sign(hyphen)  
																				    12. \.  : dot  
																					   13. \!  : exclamation mark  
																						  14. \|  : pipe  

																						   ***  

## 23. HTML  
																						   Many Markdown applications allow you to use HTML tags in Markdown-formatted text. This is helpful if you prefer certain HTML tags to Markdown syntax. For example, some people find it easier to use HTML tags for images. Using HTML is also helpful when you need to change the attributes of an element, like specifying the color of text or changing the width of an image.  
																						   To use HTML, place the tags in the text of your Markdown-formatted file.  
### Ex)  
																						   ```
																						   This **word** is bold. This <em>word</em> is italic.
																						   ```  
### Result :  
																						   This **word** is bold. This <em>word</em> is italic.  
																						   ***  

																						   [Github URL](https://github.com/aogog/Software-Engineering/blob/main/README.md)  

