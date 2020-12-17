+++
title = "Main page"
author = ["Robert Clay"]
lastmod = 2020-12-17T19:42:07+09:00
draft = false
weight = 2001
noauthor = true
nocomment = true
nodate = true
nopaging = true
noread = true
[menu.main]
  weight = 2001
  identifier = "main-page"
+++

This will be on of the pages separate from the blog posts. It will be longer

<a id="code-snippet--all-tags"></a>
```emacs-lisp
(defun flatten (list-of-lists)
  (apply #'append list-of-lists))
(let (tags)
  (org-map-entries
   (lambda ()
     (dolist (tag (org-get-tags))
       (push (list tag) tags)))
  (cl-sort tags 'string-lessp :key 'car) 'agenda-with-archives)

  (mapcar (lambda (this-tag)
                 (list this-tag (count-if (lambda (word) (string= word this-tag))(flatten tags))))
               (delete-dups (flatten tags))))
```

Here is a test for some elisp code.s
