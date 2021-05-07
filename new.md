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
