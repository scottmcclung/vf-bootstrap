##Steps to create a namespaced version of Bootstrap.
- Merge in updates from upstream repository
- Compile new namespaced copy of bootstrap using bs-prefix.less for source 
  ~~~~lessc bs-prefix.less dist/css/bs-bootstrap.css~~~~
- Replace all occurances of '.bs body' and '.bs html' with '.bs'  (you can't namespace the body and html tags)
- Compile minified copy of the namespaced bootstrap file using bs-min.less for source
  ~~~~lessc -clean-css bs-min.less dist/css/bs-bootstrap.min.css~~~~


To use, wrap content in ~~~~<div class="bs"></div>~~~~
