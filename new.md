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

