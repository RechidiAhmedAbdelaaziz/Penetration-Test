                     
                     
┌───────────────────┐
│ 196 Code Findings │
└───────────────────┘
                                                                         
  [36m[22m[24m  opencart-latest/admin/controller/catalog/download.php [0m
       [1m[24mphp.lang.security.non-literal-header.non-literal-header[0m                              
          Using user input when setting headers with `header()` is potentially dangerous. This could  
          allow an attacker to inject a new line and add a new header into the response. This is      
          called HTTP response splitting. To fix, do not allow whitespace inside `header()`: '[^\s]+'.
          Details: https://sg.run/9rL8                                                                
                                                                                                      
          492┆ [1m[24mheader('Content-Disposition: attachment; filename="' . $filename . '"')[0m;
            ⋮┆----------------------------------------
          497┆ [1m[24mheader('Content-Length: ' . filesize($file))[0m;
                                                                         
  [36m[22m[24m  opencart-latest/admin/controller/common/developer.php [0m
       [1m[24mphp.lang.security.unlink-use.unlink-use[0m                                            
          Using user input when deleting files with `unlink()` is potentially dangerous. A malicious
          actor could use this to modify or access files they have no right to.                     
          Details: https://sg.run/rYeR                                                              
                                                                                                    
           53┆ [1m[24munlink($file)[0m;
            ⋮┆----------------------------------------
           84┆ [1m[24munlink($file)[0m;
            ⋮┆----------------------------------------
           93┆ [1m[24munlink($file)[0m;
            ⋮┆----------------------------------------
          103┆ [1m[24munlink($file)[0m;
                                                                           
  [36m[22m[24m  opencart-latest/admin/controller/common/filemanager.php [0m
       [1m[24mphp.lang.security.unlink-use.unlink-use[0m                                            
          Using user input when deleting files with `unlink()` is potentially dangerous. A malicious
          actor could use this to modify or access files they have no right to.                     
          Details: https://sg.run/rYeR                                                              
                                                                                                    
          448┆ [1m[24munlink($file)[0m;
                                                                        
  [36m[22m[24m  opencart-latest/admin/controller/common/security.php [0m
       [1m[24mphp.lang.security.unlink-use.unlink-use[0m                                            
          Using user input when deleting files with `unlink()` is potentially dangerous. A malicious
          actor could use this to modify or access files they have no right to.                     
          Details: https://sg.run/rYeR                                                              
                                                                                                    
           96┆ [1m[24munlink($file)[0m;
            ⋮┆----------------------------------------
          213┆ [1m[24munlink($file)[0m;
            ⋮┆----------------------------------------
          423┆ [1m[24munlink($file)[0m;
                                                                              
  [36m[22m[24m  opencart-latest/admin/controller/marketplace/installer.php [0m
       [1m[24mphp.lang.security.unlink-use.unlink-use[0m                                            
          Using user input when deleting files with `unlink()` is potentially dangerous. A malicious
          actor could use this to modify or access files they have no right to.                     
          Details: https://sg.run/rYeR                                                              
                                                                                                    
          206┆ [1m[24munlink($this->request->files['file']['tmp_name'])[0m;
            ⋮┆----------------------------------------
          471┆ [1m[24munlink($file)[0m;
            ⋮┆----------------------------------------
          503┆ [1m[24munlink($path)[0m;
            ⋮┆----------------------------------------
          675┆ [1m[24munlink($file)[0m;
                                                                              
  [36m[22m[24m  opencart-latest/admin/controller/marketplace/promotion.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           30┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                      
  [36m[22m[24m  opencart-latest/admin/controller/startup/error.php [0m
       [1m[24mphp.lang.security.non-literal-header.non-literal-header[0m                              
          Using user input when setting headers with `header()` is potentially dangerous. This could  
          allow an attacker to inject a new line and add a new header into the response. This is      
          called HTTP response splitting. To fix, do not allow whitespace inside `header()`: '[^\s]+'.
          Details: https://sg.run/9rL8                                                                
                                                                                                      
           46┆ [1m[24mheader('Location: ' . $this->config->get('error_page'))[0m;
            ⋮┆----------------------------------------
           65┆ [1m[24mheader('Location: ' . $this->config->get('error_page'))[0m;
                                                                             
  [36m[22m[24m  opencart-latest/admin/controller/startup/notification.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           12┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                    
  [36m[22m[24m  opencart-latest/admin/controller/tool/backup.php [0m
       [1m[24mphp.lang.security.non-literal-header.non-literal-header[0m                              
          Using user input when setting headers with `header()` is potentially dangerous. This could  
          allow an attacker to inject a new line and add a new header into the response. This is      
          called HTTP response splitting. To fix, do not allow whitespace inside `header()`: '[^\s]+'.
          Details: https://sg.run/9rL8                                                                
                                                                                                      
          379┆ [1m[24mheader('Content-Disposition: attachment; filename="' . $filename . '"')[0m;
            ⋮┆----------------------------------------
          383┆ [1m[24mheader('Content-Length: ' . filesize($file))[0m;
            ⋮┆----------------------------------------
       [1m[24mphp.lang.security.unlink-use.unlink-use[0m                                            
          Using user input when deleting files with `unlink()` is potentially dangerous. A malicious
          actor could use this to modify or access files they have no right to.                     
          Details: https://sg.run/rYeR                                                              
                                                                                                    
          420┆ [1m[24munlink($file)[0m;
                                                                     
  [36m[22m[24m  opencart-latest/admin/controller/tool/upgrade.php [0m
       [1m[24mphp.lang.security.unlink-use.unlink-use[0m                                            
          Using user input when deleting files with `unlink()` is potentially dangerous. A malicious
          actor could use this to modify or access files they have no right to.                     
          Details: https://sg.run/rYeR                                                              
                                                                                                    
          188┆ [1m[24munlink(DIR_OPENCART . $destination)[0m;
                                                                    
  [36m[22m[24m  opencart-latest/admin/controller/tool/upload.php [0m
       [1m[24mphp.lang.security.non-literal-header.non-literal-header[0m                              
          Using user input when setting headers with `header()` is potentially dangerous. This could  
          allow an attacker to inject a new line and add a new header into the response. This is      
          called HTTP response splitting. To fix, do not allow whitespace inside `header()`: '[^\s]+'.
          Details: https://sg.run/9rL8                                                                
                                                                                                      
          274┆ [1m[24mheader('Content-Disposition: attachment; filename="' . ($mask ? $mask : basename($file)) .        
  '"')[0m;                                                                                                              
            ⋮┆----------------------------------------
          279┆ [1m[24mheader('Content-Length: ' . filesize($file))[0m;
            ⋮┆----------------------------------------
       [1m[24mphp.lang.security.unlink-use.unlink-use[0m                                            
          Using user input when deleting files with `unlink()` is potentially dangerous. A malicious
          actor could use this to modify or access files they have no right to.                     
          Details: https://sg.run/rYeR                                                              
                                                                                                    
          240┆ [1m[24munlink(DIR_UPLOAD . $upload_info['filename'])[0m;
                                                                                          
  [36m[22m[24m  opencart-latest/admin/view/javascript/bootstrap/js/bootstrap.bundle.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
         4921┆ [1m[24mtemplateWrapper.innerHTML = this._maybeSanitize(this._config.template);[0m
            ⋮┆----------------------------------------
         4961┆ [1m[24mtemplateElement.innerHTML = this._maybeSanitize(content);[0m
                                                                                       
  [36m[22m[24m  opencart-latest/admin/view/javascript/bootstrap/js/bootstrap.esm.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
         3078┆ [1m[24mtemplateWrapper.innerHTML = this._maybeSanitize(this._config.template);[0m
            ⋮┆----------------------------------------
         3118┆ [1m[24mtemplateElement.innerHTML = this._maybeSanitize(content);[0m
                                                                                   
  [36m[22m[24m  opencart-latest/admin/view/javascript/bootstrap/js/bootstrap.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
         3101┆ [1m[24mtemplateWrapper.innerHTML = this._maybeSanitize(this._config.template);[0m
            ⋮┆----------------------------------------
         3141┆ [1m[24mtemplateElement.innerHTML = this._maybeSanitize(content);[0m
                                                                                             
  [36m[22m[24m  opencart-latest/admin/view/javascript/ckeditor/plugins/wsc/dialogs/wsc.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
           79┆  ...                                                                                                     
  [1m[24mthis.getInputElement().$.children[0].innerHTML=a.LocalizationComing.SpellCheckingOptions[0m},children:[{type:  
  "vbox",id:"Options_checkbox",children:[{t ... [0m                                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           88┆  ...                                                                                                     
  [1m[24md.IgnoreAllCapsWords.getElement().$.lastChild.innerHTML=a.LocalizationComing.IgnoreAllCapsWords;[0m ... [0m    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           89┆                                                                                                          
  [1m[24md.IgnoreWordsNumbers.getElement().$.lastChild.innerHTML=a.LocalizationComing.IgnoreWordsWithNumbers;[0md.Igno  
  reMixedCaseWords.getElement().$.lastChild ... [0m                                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           89┆  ...                                                                                                     
  [1m[24md.IgnoreMixedCaseWords.getElement().$.lastChild.innerHTML=a.LocalizationComing.IgnoreMixedCaseWords;[0md.Igno  
  reDomainNames.getElement().$.lastChild.in ... [0m                                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           89┆  ...                                                                                                     
  [1m[24md.IgnoreDomainNames.getElement().$.lastChild.innerHTML=a.LocalizationComing.IgnoreDomainNames[0m},onHide:func  
  tion(){f.postMessage.unbindHandler(h);if( ... [0m                                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mjavascript.browser.security.wildcard-postmessage-configuration.wildcard-postmessage-   
       configuration[0m                                                                              
          The target origin of the window.postMessage() API is set to "*". This could allow for      
          information disclosure due to the possibility of any origin allowed to receive the message.
          Details: https://sg.run/PJ4p                                                               
                                                                                                     
            7┆  ...                                                                                                     
  [1m[24mf.postMessage(a,"*")[0m},unbindHandler:function(a){window.removeEventListener?window.removeEventListener("me   
  ssage",a,!1):window.detachEvent("onmessage ... [0m                                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m 
          RegExp() called with a `a` function argument, this might allow an attacker to cause a     
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the 
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your 
          regex is run on user-controlled input, consider performing input validation or use a regex
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that
          the regex does not appear vulnerable to ReDoS.                                            
          Details: https://sg.run/gr65                                                              
                                                                                                    
            7┆  ... [1m[24mnew RegExp("(?:^|; )"+a.replace(/([\.$?*|{}\(\)\[\]\\\/\+^])/g,[0m ... [0m
            8┆ [1m[24m"\\$1")+"\x3d([^;]*)")[0m))?decodeURIComponent(a[1]):void                                         
  0},remove:function(c){a(c,"",{expires:-1})}},misc:{findFocusable:function(a){var b=null;a&&( ... [0m                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m 
          RegExp() called with a `b` function argument, this might allow an attacker to cause a     
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the 
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your 
          regex is run on user-controlled input, consider performing input validation or use a regex
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that
          the regex does not appear vulnerable to ReDoS.                                            
          Details: https://sg.run/gr65                                                              
                                                                                                    
            9┆  ... [1m[24mnew                                                                                          
  RegExp("(\\s|^)"+b+"(\\s|$)")[0m))}}}}(),a=a||{};a.TextAreaNumber=null;a.load=!0;a.cmd={SpellTab:"spell",Thesaurus:"th
  es",GrammTab:"grammar"};a.di ... [0m                                                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m 
          RegExp() called with a `a` function argument, this might allow an attacker to cause a     
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the 
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your 
          regex is run on user-controlled input, consider performing input validation or use a regex
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that
          the regex does not appear vulnerable to ReDoS.                                            
          Details: https://sg.run/gr65                                                              
                                                                                                    
           42┆  ... [1m[24mnew RegExp("(?:^|;                                                                           
  )"+a.replace(/([\.$?*|{}\(\)\[\]\\\/\+^])/g,"\\$1")+"\x3d([^;]*)")[0m))?decodeURIComponent(a[1]):void                 
  0},setCookie:function(a,b,c){ ... [0m                                                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.incomplete-sanitization.incomplete-sanitization[0m       
          `a.replace` method will only replace the first occurrence when used with a string argument  
          ("["). If this method is used for escaping of dangerous data then there is a possibility for
          a bypass. Try to use sanitization library instead or use a Regex with a global flag.        
          Details: https://sg.run/1GbQ                                                                
                                                                                                      
           40┆  ... [1m[24ma.replace("[","")[0m,a=a.replace("]",""),b=""===a?[]:a.split(",")): ... [0m
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.incomplete-sanitization.incomplete-sanitization[0m       
          `a.replace` method will only replace the first occurrence when used with a string argument  
          ("]"). If this method is used for escaping of dangerous data then there is a possibility for
          a bypass. Try to use sanitization library instead or use a Regex with a global flag.        
          Details: https://sg.run/1GbQ                                                                
                                                                                                      
           40┆  ... [1m[24ma.replace("]","")[0m,b=""===a?[]:a.split(",")): ... [0m
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                      
  [36m[22m[24m  opencart-latest/admin/view/javascript/codemirror/lib/codemirror.js [0m
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m 
          RegExp() called with a `cls` function argument, this might allow an attacker to cause a   
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the 
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your 
          regex is run on user-controlled input, consider performing input validation or use a regex
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that
          the regex does not appear vulnerable to ReDoS.                                            
          Details: https://sg.run/gr65                                                              
                                                                                                    
           50┆ function classTest(cls) { return [1m[24mnew RegExp("(^|\\s)" + cls + "(?:$|\\s)\\s*")[0m }
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m 
          RegExp() called with a `type` function argument, this might allow an attacker to cause a  
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the 
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your 
          regex is run on user-controlled input, consider performing input validation or use a regex
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that
          the regex does not appear vulnerable to ReDoS.                                            
          Details: https://sg.run/gr65                                                              
                                                                                                    
         1204┆ else if (![1m[24m(new RegExp("(?:^|\\s)" + lineClass[2] + "(?:$|\\s)"))[0m.test(output[prop]))
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m 
          RegExp() called with a `val` function argument, this might allow an attacker to cause a   
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the 
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your 
          regex is run on user-controlled input, consider performing input validation or use a regex
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that
          the regex does not appear vulnerable to ReDoS.                                            
          Details: https://sg.run/gr65                                                              
                                                                                                    
         7701┆ cm.state.specialChars = [1m[24mnew RegExp(val.source + (val.test("\t") ? "" : "|\t"), "g")[0m;
                                                                                      
  [36m[22m[24m  opencart-latest/admin/view/javascript/codemirror/mode/htmlmixed.js [0m
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m 
          RegExp() called with a `attr` function argument, this might allow an attacker to cause a  
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the 
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your 
          regex is run on user-controlled input, consider performing input validation or use a regex
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that
          the regex does not appear vulnerable to ReDoS.                                            
          Details: https://sg.run/gr65                                                              
                                                                                                    
           44┆ return attrRegexpCache[attr] = [1m[24mnew RegExp("\\s+" + attr +                                         
  "\\s*=\\s*('|\")?([^'\"]+)('|\")?\\s*")[0m;                                                                           
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m  
          RegExp() called with a `tagName` function argument, this might allow an attacker to cause a
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the  
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your  
          regex is run on user-controlled input, consider performing input validation or use a regex 
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that 
          the regex does not appear vulnerable to ReDoS.                                             
          Details: https://sg.run/gr65                                                               
                                                                                                     
           53┆ return [1m[24mnew RegExp((anchored ? "^" : "") + "<\/\s*" + tagName + "\s*>", "i")[0m;
                                                                                                  
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/datetimepicker/daterangepicker.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
          158┆ [1m[24melem.innerHTML = options.locale.customRangeLabel;[0m
            ⋮┆----------------------------------------
          346┆ [1m[24melem.innerHTML = range;[0m
                                                                                         
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/datetimepicker/demo.html [0m
       [1m[24mhtml.security.audit.missing-integrity.missing-integrity[0m                             
          This tag is missing an 'integrity' subresource integrity attribute. The 'integrity'        
          attribute allows for the browser to verify that externally hosted files (for example from a
          CDN) are delivered without unexpected manipulation. Without this attribute, if an attacker 
          can modify the externally hosted resource, this could lead to XSS and other types of       
          attacks. To prevent this, include the base64-encoded cryptographic hash of the resource    
          (file) you’re telling the browser to fetch in the 'integrity' attribute for all externally 
          hosted files.                                                                              
          Details: https://sg.run/krXA                                                               
                                                                                                     
            7┆ <!--[1m[24m<link rel="stylesheet"                                                                        
  href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.0/css/bootstrap.min.css" />[0m-->                              
            ⋮┆----------------------------------------
           11┆ [1m[24m<script type="text/javascript"                                                                    
  src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.js"></script>[0m                                      
            ⋮┆----------------------------------------
           13┆ [1m[24m<script type="text/javascript"                                                                    
  src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.22.1/moment.min.js"></script>[0m                              
            ⋮┆----------------------------------------
           19┆ [1m[24m<script src="https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"></script>[0m
            ⋮┆----------------------------------------
           20┆ [1m[24m<script src="https://oss.maxcdn.com/libs/respond.js/1.4.2/respond.min.js"></script>[0m
                                                                                                      
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/datetimepicker/example/amd/index.html [0m
       [1m[24mhtml.security.audit.missing-integrity.missing-integrity[0m                             
          This tag is missing an 'integrity' subresource integrity attribute. The 'integrity'        
          attribute allows for the browser to verify that externally hosted files (for example from a
          CDN) are delivered without unexpected manipulation. Without this attribute, if an attacker 
          can modify the externally hosted resource, this could lead to XSS and other types of       
          attacks. To prevent this, include the base64-encoded cryptographic hash of the resource    
          (file) you’re telling the browser to fetch in the 'integrity' attribute for all externally 
          hosted files.                                                                              
          Details: https://sg.run/krXA                                                               
                                                                                                     
            6┆ [1m[24m<link href="http://netdna.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap.min.css"                 
  rel="stylesheet">[0m                                                                                                  
                                                                                                   
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/datetimepicker/example/amd/main.js [0m
       [1m[24mjavascript.browser.security.eval-detected.eval-detected[0m                             
          Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If
          this content can be input from outside the program, this may be a code injection           
          vulnerability. Ensure evaluated content is not definable by external sources.              
          Details: https://sg.run/7ope                                                               
                                                                                                     
           13┆ [1m[24meval($(this).val())[0m;
                                                                                                      
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/datetimepicker/example/amd/require.js [0m
       [1m[24mjavascript.browser.security.eval-detected.eval-detected[0m                             
          Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If
          this content can be input from outside the program, this may be a code injection           
          vulnerability. Ensure evaluated content is not definable by external sources.              
          Details: https://sg.run/7ope                                                               
                                                                                                     
           36┆  ... [1m[24meval(b)[0m};g(w)}})(this); ... [0m
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                             
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/datetimepicker/example/browserify/index.html [0m
       [1m[24mhtml.security.audit.missing-integrity.missing-integrity[0m                             
          This tag is missing an 'integrity' subresource integrity attribute. The 'integrity'        
          attribute allows for the browser to verify that externally hosted files (for example from a
          CDN) are delivered without unexpected manipulation. Without this attribute, if an attacker 
          can modify the externally hosted resource, this could lead to XSS and other types of       
          attacks. To prevent this, include the base64-encoded cryptographic hash of the resource    
          (file) you’re telling the browser to fetch in the 'integrity' attribute for all externally 
          hosted files.                                                                              
          Details: https://sg.run/krXA                                                               
                                                                                                     
            6┆ [1m[24m<link href="http://netdna.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap.min.css"                 
  rel="stylesheet">[0m                                                                                                  
                                                                                                          
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/datetimepicker/example/browserify/main.js [0m
       [1m[24mjavascript.browser.security.eval-detected.eval-detected[0m                             
          Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If
          this content can be input from outside the program, this may be a code injection           
          vulnerability. Ensure evaluated content is not definable by external sources.              
          Details: https://sg.run/7ope                                                               
                                                                                                     
            8┆ [1m[24meval($(this).val())[0m;
                                                                                                  
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/datetimepicker/website/index.html [0m
       [1m[24mhtml.security.audit.missing-integrity.missing-integrity[0m                             
          This tag is missing an 'integrity' subresource integrity attribute. The 'integrity'        
          attribute allows for the browser to verify that externally hosted files (for example from a
          CDN) are delivered without unexpected manipulation. Without this attribute, if an attacker 
          can modify the externally hosted resource, this could lead to XSS and other types of       
          attacks. To prevent this, include the base64-encoded cryptographic hash of the resource    
          (file) you’re telling the browser to fetch in the 'integrity' attribute for all externally 
          hosted files.                                                                              
          Details: https://sg.run/krXA                                                               
                                                                                                     
           14┆ [1m[24m<script type="text/javascript"                                                                    
  src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.22.1/moment.min.js"></script>[0m                              
            ⋮┆----------------------------------------
           15┆ [1m[24m<script type="text/javascript"                                                                    
  src="https://cdnjs.cloudflare.com/ajax/libs/trianglify/0.2.1/trianglify.min.js"></script>[0m                          
            ⋮┆----------------------------------------
           91┆ [1m[24m<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>[0m
            ⋮┆----------------------------------------
          116┆ [1m[24m<script src="https://gist.github.com/dangrossman/4879503153c6a7a0b3b6ebd64e0383b7.js"></script>[0m
            ⋮┆----------------------------------------
          125┆ [1m[24m<script src="https://gist.github.com/dangrossman/f460cf1243d8ffb08c749730e89c2f3d.js"></script>[0m
            ⋮┆----------------------------------------
          150┆ [1m[24m<script src="https://gist.github.com/dangrossman/e118af4dbadc5177d7494dba9d3295d1.js"></script>[0m
            ⋮┆----------------------------------------
          175┆ [1m[24m<script src="https://gist.github.com/dangrossman/14db17599e24652db7401ed2448eb91a.js"></script>[0m
            ⋮┆----------------------------------------
          203┆ [1m[24m<script src="https://gist.github.com/dangrossman/98d8f1c304328c191b1ad33ac21354fd.js"></script>[0m
            ⋮┆----------------------------------------
          232┆ [1m[24m<script src="https://gist.github.com/dangrossman/8c6747b82572bc860364f17258004dbb.js"></script>[0m
            ⋮┆----------------------------------------
          280┆ [1m[24m<script src="https://gist.github.com/dangrossman/d50376f3467f69e7fb5570afd07dc921.js"></script>[0m
            ⋮┆----------------------------------------
          423┆ [1m[24m<script src="https://gist.github.com/dangrossman/8ff9b1220c9b5682e8bd.js"></script>[0m
            ⋮┆----------------------------------------
          438┆ [1m[24m<script src="https://gist.github.com/dangrossman/e1a8effbaeacb50a1e31.js"></script>[0m
            ⋮┆----------------------------------------
          472┆ [1m[24m<script src="https://gist.github.com/dangrossman/1bea78da703f2896564d.js"></script>[0m
            ⋮┆----------------------------------------
          480┆ [1m[24m<script src="https://gist.github.com/dangrossman/0c6c911fea1459b5fd13.js"></script>[0m
            ⋮┆----------------------------------------
          731┆ [1m[24m<script type="text/javascript" src="https://www.w3counter.com/tracker.js?id=90840"></script>[0m
            ⋮┆----------------------------------------
       [1m[24mhtml.security.plaintext-http-link.plaintext-http-link[0m                        
          This link points to a plaintext HTTP URL. Prefer an encrypted HTTPS URL if possible.
          Details: https://sg.run/RA5q                                                        
                                                                                              
          692┆ <p>Copyright (c) 2012-2019 [1m[24m<a href="http://www.dangrossman.info">Dan Grossman</a>[0m</p>
            ⋮┆----------------------------------------
          741┆ Copyright &copy; 2012-2018 [1m[24m<a href="http://www.dangrossman.info/">Dan Grossman</a>[0m.
                                                                                                  
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/datetimepicker/website/website.js [0m
       [1m[24mjavascript.browser.security.eval-detected.eval-detected[0m                             
          Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If
          this content can be input from outside the program, this may be a code injection           
          vulnerability. Ensure evaluated content is not definable by external sources.              
          Details: https://sg.run/7ope                                                               
                                                                                                     
            4┆ [1m[24meval($(this).val())[0m;
                                                                                              
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/flot/examples/ajax/index.html [0m
       [1m[24mhtml.security.plaintext-http-link.plaintext-http-link[0m                        
          This link points to a plaintext HTTP URL. Prefer an encrypted HTTPS URL if possible.
          Details: https://sg.run/RA5q                                                        
                                                                                              
          138┆  ... [1m[24m<a                                                                                           
  href="http://epp.eurostat.ec.europa.eu/tgm/table.do?tab=table&init=1&plugin=1&language=en&pcode=tsieb020">Eurostat</a>
  [0m). Click the buttons below ... [0m                                                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                   
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/flot/examples/axes-time/index.html [0m
       [1m[24mhtml.security.plaintext-http-link.plaintext-http-link[0m                        
          This link points to a plaintext HTTP URL. Prefer an encrypted HTTPS URL if possible.
          Details: https://sg.run/RA5q                                                        
                                                                                              
          113┆  ... [1m[24m<a href="http://www.esrl.noaa.gov/gmd/ccgg/trends/">NOAA/ESRL</a>[0m).</p> ... [0m
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                      
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/flot/examples/axes-time-zones/date.js [0m
       [1m[24mjavascript.browser.security.eval-detected.eval-detected[0m                             
          Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If
          this content can be input from outside the program, this may be a code injection           
          vulnerability. Ensure evaluated content is not definable by external sources.              
          Details: https://sg.run/7ope                                                               
                                                                                                     
          784┆ data = [1m[24meval('('+ data +')')[0m;
                                                                                               
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/flot/examples/image/index.html [0m
       [1m[24mhtml.security.plaintext-http-link.plaintext-http-link[0m                        
          This link points to a plaintext HTTP URL. Prefer an encrypted HTTPS URL if possible.
          Details: https://sg.run/RA5q                                                        
                                                                                              
           56┆ <p>The Cat's Eye Nebula ([1m[24m<a href="http://hubblesite.org/gallery/album/nebula/pr2004027a/">picture 
  from Hubble</a>[0m).</p>                                                                                              
                                                                                         
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/flot/examples/index.html [0m
       [1m[24mhtml.security.plaintext-http-link.plaintext-http-link[0m                        
          This link points to a plaintext HTTP URL. Prefer an encrypted HTTPS URL if possible.
          Details: https://sg.run/RA5q                                                        
                                                                                              
           36┆ <p>Here are some examples for [1m[24m<a href="http://www.flotcharts.org">Flot</a>[0m, the Javascript     
  charting library for jQuery:</p>                                                                                      
                                                                                                     
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/flot/examples/percentiles/index.html [0m
       [1m[24mhtml.security.plaintext-http-link.plaintext-http-link[0m                        
          This link points to a plaintext HTTP URL. Prefer an encrypted HTTPS URL if possible.
          Details: https://sg.run/RA5q                                                        
                                                                                              
           68┆  ... [1m[24m<a href="http://www.cdc.gov/nchs/data/nhsr/nhsr010.pdf">CDC</a>[0m). The 15%-85%, 25%-75% and
  50% percentiles are indicated.</p> ... [0m                                                                            
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                   
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/flot/examples/selection/index.html [0m
       [1m[24mhtml.security.plaintext-http-link.plaintext-http-link[0m                        
          This link points to a plaintext HTTP URL. Prefer an encrypted HTTPS URL if possible.
          Details: https://sg.run/RA5q                                                        
                                                                                              
          117┆  ... [1m[24m<a                                                                                           
  href="http://en.wikipedia.org/wiki/List_of_countries_by_carbon_dioxide_emissions_per_capita">Wikipedia</a>[0m).</p>   
  ... [0m                                                                                                               
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                       
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/flot/examples/series-toggle/index.html [0m
       [1m[24mhtml.security.plaintext-http-link.plaintext-http-link[0m                        
          This link points to a plaintext HTTP URL. Prefer an encrypted HTTPS URL if possible.
          Details: https://sg.run/RA5q                                                        
                                                                                              
          110┆  ... [1m[24m<a href="http://www.sipri.org/">SIPRI</a>[0m).</p> ... [0m
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                               
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/flot/jquery.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
         3849┆ [1m[24mdiv.innerHTML = "<a name='" + expando + "'></a><div name='" + expando + "'></div>";[0m
            ⋮┆----------------------------------------
         5893┆ [1m[24melem.innerHTML = value;[0m
            ⋮┆----------------------------------------
         6091┆ [1m[24mdest.outerHTML = src.outerHTML;[0m
            ⋮┆----------------------------------------
         6099┆ [1m[24mdest.innerHTML = src.innerHTML;[0m
            ⋮┆----------------------------------------
         6239┆ [1m[24mfragmentDiv.innerHTML = elem.outerHTML;[0m
            ⋮┆----------------------------------------
         6325┆ [1m[24mdiv.innerHTML = wrap[1] + elem + wrap[2];[0m
            ⋮┆----------------------------------------
       [1m[24mjavascript.express.security.audit.remote-property-injection.remote-property-injection[0m
          Bracket object notation with user input is present, this might allow an attacker to access  
          all properties of the object and even it's prototype. Use literal values for object         
          properties.                                                                                 
          Details: https://sg.run/Z4gn                                                                
                                                                                                      
         9416┆ [1m[24mjQuery.fn[ funcName ] = function( margin, value ) {[0m
         9417┆ [1m[24m  var chainable = arguments.length && ( defaultExtra || typeof margin !== "boolean"    
  ),[0m                                                                                                      
         9418┆ [1m[24m          extra = defaultExtra || ( margin === true || value === true ? "margin" :     
  "border" );[0m                                                                                             
         9419┆ [1m[24m[0m
         9420┆ [1m[24m  return jQuery.access( this, function( elem, type, value )   
  {[0m                                                                              
         9421┆ [1m[24m           
  var doc;[0m                    
         9422┆ [1m[24m[0m
         9423┆ [1m[24m          if ( jQuery.isWindow(    
  elem ) ) {[0m                                          
         9424┆ [1m[24m                  // As of 5/8/2012 this will yield incorrect results for Mobile   
  Safari, but there[0m                                                                                   
         9425┆ [1m[24m                  // isn't a whole lot we can do. See pull request at this URL 
  for discussion:[0m                                                                                 
             [hid 25 additional lines, adjust with --max-lines-per-finding] 
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m 
          RegExp() called with a `types` function argument, this might allow an attacker to cause a 
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the 
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your 
          regex is run on user-controlled input, consider performing input validation or use a regex
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that
          the regex does not appear vulnerable to ReDoS.                                            
          Details: https://sg.run/gr65                                                              
                                                                                                    
         2786┆ namespaces = namespaces ? [1m[24mnew RegExp("(^|\\.)" +                                                  
  namespaces.split(".").sort().join("\\.(?:.*\\.|)") + "(\\.|$)")[0m : null;                                            
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m 
          RegExp() called with a `event` function argument, this might allow an attacker to cause a 
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the 
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your 
          regex is run on user-controlled input, consider performing input validation or use a regex
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that
          the regex does not appear vulnerable to ReDoS.                                            
          Details: https://sg.run/gr65                                                              
                                                                                                    
         2883┆ event.namespace_re = event.namespace? [1m[24mnew RegExp("(^|\\.)" + namespaces.join("\\.(?:.*\\.|)") +   
  "(\\.|$)")[0m : null;                                                                                                 
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m  
          RegExp() called with a `className` function argument, this might allow an attacker to cause
          a Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your  
          regex is run on user-controlled input, consider performing input validation or use a regex 
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that 
          the regex does not appear vulnerable to ReDoS.                                             
          Details: https://sg.run/gr65                                                               
                                                                                                     
         4261┆ (pattern = [1m[24mnew RegExp( "(^|" + whitespace + ")" + className + "(" + whitespace + "|$)" )[0m) &&
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.prototype-pollution.prototype-pollution-loop.prototype-pollution-
       loop[0m                                                                                                
          Possibility of prototype polluting function detected. By adding or modifying attributes of          
          an object prototype, it is possible to create attributes that exist on every object, or             
          replace critical attributes with malicious ones. This can be problematic if the software            
          depends on existence or non-existence of certain attributes, or uses pre-defined attributes         
          of object prototype (such as hasOwnProperty, toString or valueOf). Possible mitigations             
          might be: freezing the object prototype, using an object without prototypes (via                    
          Object.create(null) ), blocking modifications of attributes that resolve to object                  
          prototype, using Map instead of object.                                                             
          Details: https://sg.run/w1DB                                                                        
                                                                                                              
         4754┆ while [1m[24m( (elem = elem[ dir ]) )[0m {
            ⋮┆----------------------------------------
         4768┆ while [1m[24m( (elem = elem[ dir ]) )[0m {
            ⋮┆----------------------------------------
         4787┆ while [1m[24m( (elem = elem[ dir ]) )[0m {
            ⋮┆----------------------------------------
         5597┆ [1m[24mcur = cur[dir][0m;
                                                                                                    
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/jquery-ui/external/jquery/jquery.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
         6163┆ [1m[24melem.innerHTML = value;[0m
            ⋮┆----------------------------------------
         6390┆ [1m[24mdest.outerHTML = src.outerHTML;[0m
            ⋮┆----------------------------------------
         6398┆ [1m[24mdest.innerHTML = src.innerHTML;[0m
            ⋮┆----------------------------------------
         6491┆ [1m[24mfragmentDiv.innerHTML = elem.outerHTML;[0m
            ⋮┆----------------------------------------
         6569┆ [1m[24mtmp.innerHTML = wrap[1] + elem.replace( rxhtmlTag, "<$1></$2>" ) + wrap[2];[0m
            ⋮┆----------------------------------------
       [1m[24mjavascript.express.security.audit.remote-property-injection.remote-property-injection[0m
          Bracket object notation with user input is present, this might allow an attacker to access  
          all properties of the object and even it's prototype. Use literal values for object         
          properties.                                                                                 
          Details: https://sg.run/Z4gn                                                                
                                                                                                      
         9719┆ [1m[24mjQuery.fn[ funcName ] = function( margin, value ) {[0m
         9720┆ [1m[24m  var chainable = arguments.length && ( defaultExtra || typeof margin !== "boolean"    
  ),[0m                                                                                                      
         9721┆ [1m[24m          extra = defaultExtra || ( margin === true || value === true ? "margin" :     
  "border" );[0m                                                                                             
         9722┆ [1m[24m[0m
         9723┆ [1m[24m  return jQuery.access( this, function( elem, type, value )   
  {[0m                                                                              
         9724┆ [1m[24m           
  var doc;[0m                    
         9725┆ [1m[24m[0m
         9726┆ [1m[24m          if ( jQuery.isWindow(    
  elem ) ) {[0m                                          
         9727┆ [1m[24m                  // As of 5/8/2012 this will yield incorrect results for Mobile   
  Safari, but there[0m                                                                                   
         9728┆ [1m[24m                  // isn't a whole lot we can do. See pull request at this URL 
  for discussion:[0m                                                                                 
             [hid 25 additional lines, adjust with --max-lines-per-finding] 
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m  
          RegExp() called with a `className` function argument, this might allow an attacker to cause
          a Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your  
          regex is run on user-controlled input, consider performing input validation or use a regex 
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that 
          the regex does not appear vulnerable to ReDoS.                                             
          Details: https://sg.run/gr65                                                               
                                                                                                     
         2027┆ (pattern = [1m[24mnew RegExp( "(^|" + whitespace + ")" + className + "(" + whitespace + "|$)" )[0m) &&
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m 
          RegExp() called with a `types` function argument, this might allow an attacker to cause a 
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the 
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your 
          regex is run on user-controlled input, consider performing input validation or use a regex
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that
          the regex does not appear vulnerable to ReDoS.                                            
          Details: https://sg.run/gr65                                                              
                                                                                                    
         4878┆ tmp = tmp[2] && [1m[24mnew RegExp( "(^|\\.)" + namespaces.join("\\.(?:.*\\.|)") + "(\\.|$)" )[0m;
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m 
          RegExp() called with a `event` function argument, this might allow an attacker to cause a 
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the 
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your 
          regex is run on user-controlled input, consider performing input validation or use a regex
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that
          the regex does not appear vulnerable to ReDoS.                                            
          Details: https://sg.run/gr65                                                              
                                                                                                    
         4957┆ [1m[24mnew RegExp( "(^|\\.)" + namespaces.join("\\.(?:.*\\.|)") + "(\\.|$)" )[0m :
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.prototype-pollution.prototype-pollution-loop.prototype-pollution-
       loop[0m                                                                                                
          Possibility of prototype polluting function detected. By adding or modifying attributes of          
          an object prototype, it is possible to create attributes that exist on every object, or             
          replace critical attributes with malicious ones. This can be problematic if the software            
          depends on existence or non-existence of certain attributes, or uses pre-defined attributes         
          of object prototype (such as hasOwnProperty, toString or valueOf). Possible mitigations             
          might be: freezing the object prototype, using an object without prototypes (via                    
          Object.create(null) ), blocking modifications of attributes that resolve to object                  
          prototype, using Map instead of object.                                                             
          Details: https://sg.run/w1DB                                                                        
                                                                                                              
         2082┆ while [1m[24m( (node = node[ dir ]) )[0m {
            ⋮┆----------------------------------------
         2483┆ while [1m[24m( (elem = elem[ dir ]) )[0m {
            ⋮┆----------------------------------------
         2497┆ while [1m[24m( (elem = elem[ dir ]) )[0m {
            ⋮┆----------------------------------------
         2505┆ while [1m[24m( (elem = elem[ dir ]) )[0m {
            ⋮┆----------------------------------------
         5937┆ [1m[24mcur = cur[dir][0m;
                                                                                       
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/jquery-ui/jquery-ui.js [0m
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m  
          RegExp() called with a `character` function argument, this might allow an attacker to cause
          a Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your  
          regex is run on user-controlled input, consider performing input validation or use a regex 
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that 
          the regex does not appear vulnerable to ReDoS.                                             
          Details: https://sg.run/gr65                                                               
                                                                                                     
         6968┆ regex = [1m[24mnew RegExp( "^" + escapedCharacter, "i" )[0m;
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.detect-non-literal-regexp.detect-non-literal-regexp[0m 
          RegExp() called with a `term` function argument, this might allow an attacker to cause a  
          Regular Expression Denial-of-Service (ReDoS) within your application as RegExP blocks the 
          main thread. For this reason, it is recommended to use hardcoded regexes instead. If your 
          regex is run on user-controlled input, consider performing input validation or use a regex
          checking/sanitization library such as https://www.npmjs.com/package/recheck to verify that
          the regex does not appear vulnerable to ReDoS.                                            
          Details: https://sg.run/gr65                                                              
                                                                                                    
         7554┆ var matcher = [1m[24mnew RegExp( $.ui.autocomplete.escapeRegex( term ), "i" )[0m;
            ⋮┆----------------------------------------
       [1m[24mjavascript.lang.security.audit.prototype-pollution.prototype-pollution-loop.prototype-pollution-
       loop[0m                                                                                                
          Possibility of prototype polluting function detected. By adding or modifying attributes of          
          an object prototype, it is possible to create attributes that exist on every object, or             
          replace critical attributes with malicious ones. This can be problematic if the software            
          depends on existence or non-existence of certain attributes, or uses pre-defined attributes         
          of object prototype (such as hasOwnProperty, toString or valueOf). Possible mitigations             
          might be: freezing the object prototype, using an object without prototypes (via                    
          Object.create(null) ), blocking modifications of attributes that resolve to object                  
          prototype, using Map instead of object.                                                             
          Details: https://sg.run/w1DB                                                                        
                                                                                                              
          642┆ [1m[24mcurOption = curOption[ parts[ i ] ][0m;
                                                                                                  
  [36m[22m[24m  opencart-latest/admin/view/javascript/jquery/magnific/jquery.magnific-popup.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
           67┆ [1m[24mel.innerHTML = html;[0m
                                                                           
  [36m[22m[24m  opencart-latest/catalog/controller/account/download.php [0m
       [1m[24mphp.lang.security.non-literal-header.non-literal-header[0m                              
          Using user input when setting headers with `header()` is potentially dangerous. This could  
          allow an attacker to inject a new line and add a new header into the response. This is      
          called HTTP response splitting. To fix, do not allow whitespace inside `header()`: '[^\s]+'.
          Details: https://sg.run/9rL8                                                                
                                                                                                      
          126┆ [1m[24mheader('Content-Disposition: attachment; filename="' . ($mask ? $mask : basename($file)) .        
  '"')[0m;                                                                                                              
            ⋮┆----------------------------------------
          130┆ [1m[24mheader('Content-Length: ' . filesize($file))[0m;
                                                                        
  [36m[22m[24m  opencart-latest/catalog/controller/startup/error.php [0m
       [1m[24mphp.lang.security.non-literal-header.non-literal-header[0m                              
          Using user input when setting headers with `header()` is potentially dangerous. This could  
          allow an attacker to inject a new line and add a new header into the response. This is      
          called HTTP response splitting. To fix, do not allow whitespace inside `header()`: '[^\s]+'.
          Details: https://sg.run/9rL8                                                                
                                                                                                      
           42┆ [1m[24mheader('Location: ' . $this->config->get('error_page'))[0m;
            ⋮┆----------------------------------------
           57┆ [1m[24mheader('Location: ' . $this->config->get('error_page'))[0m;
                                                                                            
  [36m[22m[24m  opencart-latest/catalog/view/javascript/bootstrap/js/bootstrap.bundle.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
         4921┆ [1m[24mtemplateWrapper.innerHTML = this._maybeSanitize(this._config.template);[0m
            ⋮┆----------------------------------------
         4961┆ [1m[24mtemplateElement.innerHTML = this._maybeSanitize(content);[0m
                                                                                         
  [36m[22m[24m  opencart-latest/catalog/view/javascript/bootstrap/js/bootstrap.esm.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
         3078┆ [1m[24mtemplateWrapper.innerHTML = this._maybeSanitize(this._config.template);[0m
            ⋮┆----------------------------------------
         3118┆ [1m[24mtemplateElement.innerHTML = this._maybeSanitize(content);[0m
                                                                                     
  [36m[22m[24m  opencart-latest/catalog/view/javascript/bootstrap/js/bootstrap.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
         3101┆ [1m[24mtemplateWrapper.innerHTML = this._maybeSanitize(this._config.template);[0m
            ⋮┆----------------------------------------
         3141┆ [1m[24mtemplateElement.innerHTML = this._maybeSanitize(content);[0m
                                                                                                    
  [36m[22m[24m  opencart-latest/catalog/view/javascript/jquery/datetimepicker/daterangepicker.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
          158┆ [1m[24melem.innerHTML = options.locale.customRangeLabel;[0m
            ⋮┆----------------------------------------
          346┆ [1m[24melem.innerHTML = range;[0m
                                                                                           
  [36m[22m[24m  opencart-latest/catalog/view/javascript/jquery/datetimepicker/demo.html [0m
       [1m[24mhtml.security.audit.missing-integrity.missing-integrity[0m                             
          This tag is missing an 'integrity' subresource integrity attribute. The 'integrity'        
          attribute allows for the browser to verify that externally hosted files (for example from a
          CDN) are delivered without unexpected manipulation. Without this attribute, if an attacker 
          can modify the externally hosted resource, this could lead to XSS and other types of       
          attacks. To prevent this, include the base64-encoded cryptographic hash of the resource    
          (file) you’re telling the browser to fetch in the 'integrity' attribute for all externally 
          hosted files.                                                                              
          Details: https://sg.run/krXA                                                               
                                                                                                     
            7┆ <!--[1m[24m<link rel="stylesheet"                                                                        
  href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.0/css/bootstrap.min.css" />[0m-->                              
            ⋮┆----------------------------------------
           11┆ [1m[24m<script type="text/javascript"                                                                    
  src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.js"></script>[0m                                      
            ⋮┆----------------------------------------
           13┆ [1m[24m<script type="text/javascript"                                                                    
  src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.22.1/moment.min.js"></script>[0m                              
            ⋮┆----------------------------------------
           19┆ [1m[24m<script src="https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"></script>[0m
            ⋮┆----------------------------------------
           20┆ [1m[24m<script src="https://oss.maxcdn.com/libs/respond.js/1.4.2/respond.min.js"></script>[0m
                                                                                                        
  [36m[22m[24m  opencart-latest/catalog/view/javascript/jquery/datetimepicker/example/amd/index.html [0m
       [1m[24mhtml.security.audit.missing-integrity.missing-integrity[0m                             
          This tag is missing an 'integrity' subresource integrity attribute. The 'integrity'        
          attribute allows for the browser to verify that externally hosted files (for example from a
          CDN) are delivered without unexpected manipulation. Without this attribute, if an attacker 
          can modify the externally hosted resource, this could lead to XSS and other types of       
          attacks. To prevent this, include the base64-encoded cryptographic hash of the resource    
          (file) you’re telling the browser to fetch in the 'integrity' attribute for all externally 
          hosted files.                                                                              
          Details: https://sg.run/krXA                                                               
                                                                                                     
            6┆ [1m[24m<link href="http://netdna.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap.min.css"                 
  rel="stylesheet">[0m                                                                                                  
                                                                                                     
  [36m[22m[24m  opencart-latest/catalog/view/javascript/jquery/datetimepicker/example/amd/main.js [0m
       [1m[24mjavascript.browser.security.eval-detected.eval-detected[0m                             
          Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If
          this content can be input from outside the program, this may be a code injection           
          vulnerability. Ensure evaluated content is not definable by external sources.              
          Details: https://sg.run/7ope                                                               
                                                                                                     
           13┆ [1m[24meval($(this).val())[0m;
                                                                                                        
  [36m[22m[24m  opencart-latest/catalog/view/javascript/jquery/datetimepicker/example/amd/require.js [0m
       [1m[24mjavascript.browser.security.eval-detected.eval-detected[0m                             
          Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If
          this content can be input from outside the program, this may be a code injection           
          vulnerability. Ensure evaluated content is not definable by external sources.              
          Details: https://sg.run/7ope                                                               
                                                                                                     
           36┆  ... [1m[24meval(b)[0m};g(w)}})(this); ... [0m
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                               
  [36m[22m[24m  opencart-latest/catalog/view/javascript/jquery/datetimepicker/example/browserify/index.html [0m
       [1m[24mhtml.security.audit.missing-integrity.missing-integrity[0m                             
          This tag is missing an 'integrity' subresource integrity attribute. The 'integrity'        
          attribute allows for the browser to verify that externally hosted files (for example from a
          CDN) are delivered without unexpected manipulation. Without this attribute, if an attacker 
          can modify the externally hosted resource, this could lead to XSS and other types of       
          attacks. To prevent this, include the base64-encoded cryptographic hash of the resource    
          (file) you’re telling the browser to fetch in the 'integrity' attribute for all externally 
          hosted files.                                                                              
          Details: https://sg.run/krXA                                                               
                                                                                                     
            6┆ [1m[24m<link href="http://netdna.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap.min.css"                 
  rel="stylesheet">[0m                                                                                                  
                                                                                                            
  [36m[22m[24m  opencart-latest/catalog/view/javascript/jquery/datetimepicker/example/browserify/main.js [0m
       [1m[24mjavascript.browser.security.eval-detected.eval-detected[0m                             
          Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If
          this content can be input from outside the program, this may be a code injection           
          vulnerability. Ensure evaluated content is not definable by external sources.              
          Details: https://sg.run/7ope                                                               
                                                                                                     
            8┆ [1m[24meval($(this).val())[0m;
                                                                                                    
  [36m[22m[24m  opencart-latest/catalog/view/javascript/jquery/datetimepicker/website/index.html [0m
       [1m[24mhtml.security.audit.missing-integrity.missing-integrity[0m                             
          This tag is missing an 'integrity' subresource integrity attribute. The 'integrity'        
          attribute allows for the browser to verify that externally hosted files (for example from a
          CDN) are delivered without unexpected manipulation. Without this attribute, if an attacker 
          can modify the externally hosted resource, this could lead to XSS and other types of       
          attacks. To prevent this, include the base64-encoded cryptographic hash of the resource    
          (file) you’re telling the browser to fetch in the 'integrity' attribute for all externally 
          hosted files.                                                                              
          Details: https://sg.run/krXA                                                               
                                                                                                     
           14┆ [1m[24m<script type="text/javascript"                                                                    
  src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.22.1/moment.min.js"></script>[0m                              
            ⋮┆----------------------------------------
           15┆ [1m[24m<script type="text/javascript"                                                                    
  src="https://cdnjs.cloudflare.com/ajax/libs/trianglify/0.2.1/trianglify.min.js"></script>[0m                          
            ⋮┆----------------------------------------
           91┆ [1m[24m<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>[0m
            ⋮┆----------------------------------------
          116┆ [1m[24m<script src="https://gist.github.com/dangrossman/4879503153c6a7a0b3b6ebd64e0383b7.js"></script>[0m
            ⋮┆----------------------------------------
          125┆ [1m[24m<script src="https://gist.github.com/dangrossman/f460cf1243d8ffb08c749730e89c2f3d.js"></script>[0m
            ⋮┆----------------------------------------
          150┆ [1m[24m<script src="https://gist.github.com/dangrossman/e118af4dbadc5177d7494dba9d3295d1.js"></script>[0m
            ⋮┆----------------------------------------
          175┆ [1m[24m<script src="https://gist.github.com/dangrossman/14db17599e24652db7401ed2448eb91a.js"></script>[0m
            ⋮┆----------------------------------------
          203┆ [1m[24m<script src="https://gist.github.com/dangrossman/98d8f1c304328c191b1ad33ac21354fd.js"></script>[0m
            ⋮┆----------------------------------------
          232┆ [1m[24m<script src="https://gist.github.com/dangrossman/8c6747b82572bc860364f17258004dbb.js"></script>[0m
            ⋮┆----------------------------------------
          280┆ [1m[24m<script src="https://gist.github.com/dangrossman/d50376f3467f69e7fb5570afd07dc921.js"></script>[0m
            ⋮┆----------------------------------------
          423┆ [1m[24m<script src="https://gist.github.com/dangrossman/8ff9b1220c9b5682e8bd.js"></script>[0m
            ⋮┆----------------------------------------
          438┆ [1m[24m<script src="https://gist.github.com/dangrossman/e1a8effbaeacb50a1e31.js"></script>[0m
            ⋮┆----------------------------------------
          472┆ [1m[24m<script src="https://gist.github.com/dangrossman/1bea78da703f2896564d.js"></script>[0m
            ⋮┆----------------------------------------
          480┆ [1m[24m<script src="https://gist.github.com/dangrossman/0c6c911fea1459b5fd13.js"></script>[0m
            ⋮┆----------------------------------------
          731┆ [1m[24m<script type="text/javascript" src="https://www.w3counter.com/tracker.js?id=90840"></script>[0m
            ⋮┆----------------------------------------
       [1m[24mhtml.security.plaintext-http-link.plaintext-http-link[0m                        
          This link points to a plaintext HTTP URL. Prefer an encrypted HTTPS URL if possible.
          Details: https://sg.run/RA5q                                                        
                                                                                              
          692┆ <p>Copyright (c) 2012-2019 [1m[24m<a href="http://www.dangrossman.info">Dan Grossman</a>[0m</p>
            ⋮┆----------------------------------------
          741┆ Copyright &copy; 2012-2018 [1m[24m<a href="http://www.dangrossman.info/">Dan Grossman</a>[0m.
                                                                                                    
  [36m[22m[24m  opencart-latest/catalog/view/javascript/jquery/datetimepicker/website/website.js [0m
       [1m[24mjavascript.browser.security.eval-detected.eval-detected[0m                             
          Detected the use of eval(). eval() can be dangerous if used to evaluate dynamic content. If
          this content can be input from outside the program, this may be a code injection           
          vulnerability. Ensure evaluated content is not definable by external sources.              
          Details: https://sg.run/7ope                                                               
                                                                                                     
            4┆ [1m[24meval($(this).val())[0m;
                                                                                                    
  [36m[22m[24m  opencart-latest/catalog/view/javascript/jquery/magnific/jquery.magnific-popup.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
           67┆ [1m[24mel.innerHTML = html;[0m
                                            
  [36m[22m[24m  opencart-latest/cron.php [0m
       [1m[24mphp.lang.security.non-literal-header.non-literal-header[0m                              
          Using user input when setting headers with `header()` is potentially dangerous. This could  
          allow an attacker to inject a new line and add a new header into the response. This is      
          called HTTP response splitting. To fix, do not allow whitespace inside `header()`: '[^\s]+'.
          Details: https://sg.run/9rL8                                                                
                                                                                                      
           77┆ [1m[24mheader('Location: ' . $config->get('error_page'))[0m;
            ⋮┆----------------------------------------
           93┆ [1m[24mheader('Location: ' . $config->get('error_page'))[0m;
                                                                                        
  [36m[22m[24m  opencart-latest/extension/opencart/admin/controller/currency/ecb.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           66┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                                          
  [36m[22m[24m  opencart-latest/extension/opencart/admin/controller/currency/fixer.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           71┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                                          
  [36m[22m[24m  opencart-latest/extension/opencart/catalog/controller/currency/ecb.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           11┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                                            
  [36m[22m[24m  opencart-latest/extension/opencart/catalog/controller/currency/fixer.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           11┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                            
  [36m[22m[24m  opencart-latest/install/controller/install/promotion.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           10┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                            
  [36m[22m[24m  opencart-latest/install/controller/upgrade/upgrade_1.php [0m
       [1m[24mphp.lang.security.unlink-use.unlink-use[0m                                            
          Using user input when deleting files with `unlink()` is potentially dangerous. A malicious
          actor could use this to modify or access files they have no right to.                     
          Details: https://sg.run/rYeR                                                              
                                                                                                    
          224┆ [1m[24munlink($delete)[0m;
            ⋮┆----------------------------------------
          372┆ [1m[24munlink($file)[0m;
            ⋮┆----------------------------------------
          417┆ @[1m[24munlink($file)[0m;
                                                                            
  [36m[22m[24m  opencart-latest/install/controller/upgrade/upgrade_2.php [0m
       [1m[24mphp.lang.security.unlink-use.unlink-use[0m                                            
          Using user input when deleting files with `unlink()` is potentially dangerous. A malicious
          actor could use this to modify or access files they have no right to.                     
          Details: https://sg.run/rYeR                                                              
                                                                                                    
           99┆ [1m[24munlink($base . $destination)[0m;
            ⋮┆----------------------------------------
          135┆ [1m[24munlink($file)[0m;
                                                                            
  [36m[22m[24m  opencart-latest/install/controller/upgrade/upgrade_4.php [0m
       [1m[24mphp.lang.security.unserialize-use.unserialize-use[0m                                    
          Calling `unserialize()` with user input in the pattern can lead to arbitrary code execution.
          Consider using JSON or structured data approaches (e.g. Google Protocol Buffers).           
          Details: https://sg.run/b24E                                                                
                                                                                                      
           26┆  ... [1m[24munserialize($result['value'])[0m)) . "' WHERE `setting_id` = '" . (int)$result['setting_id'] 
  . "'"); ... [0m                                                                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                            
  [36m[22m[24m  opencart-latest/install/controller/upgrade/upgrade_6.php [0m
       [1m[24mphp.lang.security.unserialize-use.unserialize-use[0m                                    
          Calling `unserialize()` with user input in the pattern can lead to arbitrary code execution.
          Consider using JSON or structured data approaches (e.g. Google Protocol Buffers).           
          Details: https://sg.run/b24E                                                                
                                                                                                      
           16┆  ... [1m[24munserialize($result['custom_field'])[0m)) . "' WHERE `customer_id` = '" .                    
  (int)$result['customer_id'] . "'"); ... [0m                                                                           
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           25┆  ... [1m[24munserialize($result['data'])[0m)) . "' WHERE `customer_activity_id` = '" .                   
  (int)$result['customer_activity_id'] . "'"); ... [0m                                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           34┆  ... [1m[24munserialize($result['custom_field'])[0m)) . "' WHERE `address_id` = '" .                     
  (int)$result['address_id'] . "'"); ... [0m                                                                            
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           43┆  ... [1m[24munserialize($result['setting'])[0m)) . "' WHERE `module_id` = '" . (int)$result['module_id'] 
  . "'"); ... [0m                                                                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           52┆  ... [1m[24munserialize($result['custom_field'])[0m)) . "' WHERE `order_id` = '" .                       
  (int)$result['order_id'] . "'"); ... [0m                                                                              
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           56┆  ... [1m[24munserialize($result['payment_custom_field'])[0m)) . "' WHERE `order_id` = '" .               
  (int)$result['order_id'] . "'"); ... [0m                                                                              
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           60┆  ... [1m[24munserialize($result['shipping_custom_field'])[0m)) . "' WHERE `order_id` = '" .              
  (int)$result['order_id'] . "'"); ... [0m                                                                              
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           69┆  ... [1m[24munserialize($result['permission'])[0m)) . "' WHERE `user_group_id` = '" .                    
  (int)$result['user_group_id'] . "'"); ... [0m                                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                            
  [36m[22m[24m  opencart-latest/install/view/javascript/bootstrap/js/bootstrap.bundle.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
         4921┆ [1m[24mtemplateWrapper.innerHTML = this._maybeSanitize(this._config.template);[0m
            ⋮┆----------------------------------------
         4961┆ [1m[24mtemplateElement.innerHTML = this._maybeSanitize(content);[0m
                                                                                         
  [36m[22m[24m  opencart-latest/install/view/javascript/bootstrap/js/bootstrap.esm.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
         3078┆ [1m[24mtemplateWrapper.innerHTML = this._maybeSanitize(this._config.template);[0m
            ⋮┆----------------------------------------
         3118┆ [1m[24mtemplateElement.innerHTML = this._maybeSanitize(content);[0m
                                                                                     
  [36m[22m[24m  opencart-latest/install/view/javascript/bootstrap/js/bootstrap.js [0m
       [1m[24mjavascript.browser.security.insecure-document-method.insecure-document-method[0m   
          User controlled data in methods like `innerHTML`, `outerHTML` or `document.write` is an
          anti-pattern that can lead to XSS vulnerabilities                                      
          Details: https://sg.run/LwA9                                                           
                                                                                                 
         3101┆ [1m[24mtemplateWrapper.innerHTML = this._maybeSanitize(this._config.template);[0m
            ⋮┆----------------------------------------
         3141┆ [1m[24mtemplateElement.innerHTML = this._maybeSanitize(content);[0m
                                                        
  [36m[22m[24m  opencart-latest/system/framework.php [0m
       [1m[24mphp.lang.security.non-literal-header.non-literal-header[0m                              
          Using user input when setting headers with `header()` is potentially dangerous. This could  
          allow an attacker to inject a new line and add a new header into the response. This is      
          called HTTP response splitting. To fix, do not allow whitespace inside `header()`: '[^\s]+'.
          Details: https://sg.run/9rL8                                                                
                                                                                                      
           65┆ [1m[24mheader('Location: ' . $config->get('error_page'))[0m;
            ⋮┆----------------------------------------
           81┆ [1m[24mheader('Location: ' . $config->get('error_page'))[0m;
                                                                 
  [36m[22m[24m  opencart-latest/system/library/cache/file.php [0m
       [1m[24mphp.lang.security.unlink-use.unlink-use[0m                                            
          Using user input when deleting files with `unlink()` is potentially dangerous. A malicious
          actor could use this to modify or access files they have no right to.                     
          Details: https://sg.run/rYeR                                                              
                                                                                                    
           62┆ if (!@[1m[24munlink($file)[0m) {
            ⋮┆----------------------------------------
           80┆ if (!@[1m[24munlink($file)[0m) {
                                                                    
  [36m[22m[24m  opencart-latest/system/library/cart/customer.php [0m
       [1m[24mphp.lang.security.md5-loose-equality.md5-loose-equality[0m                          
          Make sure comparisons involving md5 values are strict (use `===` not `==`) to avoid type
          juggling issues                                                                         
          Details: https://sg.run/Do4G                                                            
                                                                                                  
           64┆ } elseif ([1m[24m$customer_query->row['password'] == md5($password)[0m) {
                                                                
  [36m[22m[24m  opencart-latest/system/library/cart/user.php [0m
       [1m[24mphp.lang.security.md5-loose-equality.md5-loose-equality[0m                          
          Make sure comparisons involving md5 values are strict (use `===` not `==`) to avoid type
          juggling issues                                                                         
          Details: https://sg.run/Do4G                                                            
                                                                                                  
           65┆ } elseif ([1m[24m$user_query->row['password'] == md5($password)[0m) {
                                                                 
  [36m[22m[24m  opencart-latest/system/library/encryption.php [0m
       [1m[24mphp.lang.security.audit.openssl-decrypt-validate.openssl-decrypt-validate[0m          
          The function `openssl_decrypt` returns either a string of the decrypted data on success or
          `false` on failure. If the failure case is not handled, this could lead to undefined      
          behavior in your application. Please handle the case where `openssl_decrypt` returns      
          `false`.                                                                                  
          Details: https://sg.run/kzn7                                                              
                                                                                                    
           52┆ [1m[24m$result = openssl_decrypt($value, $this->cipher, $key, OPENSSL_RAW_DATA, $iv);[0m
                                                               
  [36m[22m[24m  opencart-latest/system/library/response.php [0m
       [1m[24mphp.lang.security.non-literal-header.non-literal-header[0m                              
          Using user input when setting headers with `header()` is potentially dangerous. This could  
          allow an attacker to inject a new line and add a new header into the response. This is      
          called HTTP response splitting. To fix, do not allow whitespace inside `header()`: '[^\s]+'.
          Details: https://sg.run/9rL8                                                                
                                                                                                      
           50┆ [1m[24mheader('Location: ' . str_replace(['&amp;', "\n", "\r"], ['&', '', ''], $url), true, $status)[0m;
            ⋮┆----------------------------------------
          130┆ [1m[24mheader($header, true)[0m;
                                                                   
  [36m[22m[24m  opencart-latest/system/library/session/file.php [0m
       [1m[24mphp.lang.security.unlink-use.unlink-use[0m                                            
          Using user input when deleting files with `unlink()` is potentially dangerous. A malicious
          actor could use this to modify or access files they have no right to.                     
          Details: https://sg.run/rYeR                                                              
                                                                                                    
           56┆ [1m[24munlink($file)[0m;
            ⋮┆----------------------------------------
           73┆ [1m[24munlink($file)[0m;
