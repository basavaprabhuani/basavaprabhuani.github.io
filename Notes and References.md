```diff

!Functions and Meanings of all the files: 
-    _config.yml:
+       Deals with the entire layout and backbone of the website. Controls certain variables, like 'email, X id', etc. Controls the theme, layout, title, font, etc. 
    
-    -index.markdown:
+        Contains the text to be written in the top portion, that is, the introduction/entry to the website. 
    
-    {filename}.md:
+        These files are the separate webpages within the website as links to another webpage, like About Me, Contact, Support, etc.
    
-    _posts folder:
+        Contains the content under 'Posts' category. Add content to this using the file existing in _posts by default, as a boilerplate. 
    
-    _site and .gitignore: 
+        DON'T MESS WITH THESE FILES, THESE CANNOT BE CONTROLLED 

 
!Commands of GitBash: 
-    cd {insert/file/location/here}:
+        Takes control/performs commands on the files of folder opened using the cd command. 
    
-    bundle exec jekyll serve:
+        Launches the website locally, to preview it before pushing it to the main branch. 
        
-    pwd -W:
+        Prints out the directory of the current folder it is working in. 

The actual styling logic lives in root/assets/main.scss, and Jekyll automatically compiles this into _site/assets/main.css.
So although the HTML links to /assets/main.css, the source of truth is main.scss in the root-level assets/ folder.

✅ You only ever need to edit main.scss — Jekyll takes care of the rest.

