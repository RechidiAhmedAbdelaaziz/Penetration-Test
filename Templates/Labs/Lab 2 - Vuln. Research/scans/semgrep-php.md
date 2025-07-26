                     
                     
┌───────────────────┐
│ 921 Code Findings │
└───────────────────┘
                                                                                            
  [36m[22m[24m  /var/www/html/opencart-latest/admin/controller/marketplace/promotion.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           30┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                                           
  [36m[22m[24m  /var/www/html/opencart-latest/admin/controller/startup/notification.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           12┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                                         
  [36m[22m[24m  /var/www/html/opencart-latest/admin/language/en-gb/catalog/option.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           11┆ [1m[24m$_['text_select']        = 'Select';[0m
                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/admin/language/en-gb/catalog/product.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           21┆ [1m[24m$_['text_select']             = 'Select';[0m
                                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/admin/language/en-gb/customer/custom_field.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           11┆ [1m[24m$_['text_select']          = 'Select';[0m
                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/admin/language/en-gb/default.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           21┆ [1m[24m$_['text_select_all']               = 'Select All';[0m
                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/admin/language/en-gb/setting/setting.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
          227┆ [1m[24m$_['help_mail_alert']                     = 'Select which features you would like to receive an   
  alert email on when a customer uses them.';[0m                                                                        
                                                                                   
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/catalog/attribute.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           83┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "attribute` a LEFT JOIN `" . DB_PREFIX .
  "attribute_description` ad ON (a.`attribute_id` = ad ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          157┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "attribute_description` WHERE           
  `attribute_id` = '" . (int)$attribute_id . "'");[0m                                                                   
            ⋮┆----------------------------------------
          193┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "attribute` WHERE     
  `attribute_group_id` = '" . (int)$attribute_group_id . "' ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           83┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "attribute` a LEFT JOIN `" . DB_PREFIX .
  "attribute_description` ad ON (a.`attribute_id` = ad ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           99┆ [1m[24m$sql = "SELECT *, (SELECT agd.`name` FROM `" . DB_PREFIX . "attribute_group_description` agd WHERE
  agd.`attribute_group_id` = a.`attribute_group_id` AN ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          157┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "attribute_description` WHERE           
  `attribute_id` = '" . (int)$attribute_id . "'");[0m                                                                   
            ⋮┆----------------------------------------
          174┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "attribute`");[0m
            ⋮┆----------------------------------------
          193┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "attribute` WHERE     
  `attribute_group_id` = '" . (int)$attribute_group_id . "' ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                         
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/catalog/attribute_group.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           32┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "attribute_group` WHERE                 
  `attribute_group_id` = '" . (int)$attribute_group_id . "'");[0m                                                       
            ⋮┆----------------------------------------
           77┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "attribute_group_description` WHERE     
  `attribute_group_id` = '" . (int)$attribute_group_id . "' ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           32┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "attribute_group` WHERE                 
  `attribute_group_id` = '" . (int)$attribute_group_id . "'");[0m                                                       
            ⋮┆----------------------------------------
           38┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "attribute_group` ag LEFT JOIN `" . DB_PREFIX .            
  "attribute_group_description` agd ON (ag.`attribute_group_id` =  ... [0m                                              
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           77┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "attribute_group_description` WHERE     
  `attribute_group_id` = '" . (int)$attribute_group_id . "' ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           87┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX .                       
  "attribute_group`");[0m                                                                                               
                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/catalog/category.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$this->db->query("INSERT INTO `" . DB_PREFIX . "category` SET `parent_id` = '" .                  
  (int)$data['parent_id'] . "', `top` = '" . (isset($data['top']) ? (int ... [0m                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           10┆ [1m[24m$this->db->query("UPDATE `" . DB_PREFIX . "category` SET `image` = '" .                           
  $this->db->escape((string)$data['image']) . "' WHERE `category_id` = '" . (int) ... [0m                               
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           20┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '"
  . (int)$data['parent_id'] . "' ORDER BY `level` ASC" ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           76┆ [1m[24m$this->db->query("UPDATE `" . DB_PREFIX . "category` SET `parent_id` = '" .                       
  (int)$data['parent_id'] . "', `top` = '" . (isset($data['top']) ? (int)$dat ... [0m                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$this->db->query("UPDATE `" . DB_PREFIX . "category` SET `image` = '" .                           
  $this->db->escape((string)$data['image']) . "' WHERE `category_id` = '" . (int) ... [0m                               
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           82┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "category_description` WHERE `category_id` = '" .  
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
           85┆ [1m[24m$this->db->query("INSERT INTO `" . DB_PREFIX . "category_description` SET `category_id` = '" .    
  (int)$category_id . "', `language_id` = '" . (int)$langu ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           92┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `path_id` = '" .  
  (int)$category_id . "' ORDER BY `level` ASC");[0m                                                                     
            ⋮┆----------------------------------------
          102┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '"
  . (int)$data['parent_id'] . "' ORDER BY `level` ASC" ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          126┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '" .         
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          131┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '"
  . (int)$data['parent_id'] . "' ORDER BY `level` ASC" ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          134┆ [1m[24m$this->db->query("INSERT INTO `" . DB_PREFIX . "category_path` SET `category_id` = '" .           
  (int)$category_id . "', `path_id` = '" . (int)$result['path_id' ... [0m                                               
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          139┆ [1m[24m$this->db->query("REPLACE INTO `" . DB_PREFIX . "category_path` SET `category_id` = '" .          
  (int)$category_id . "', `path_id` = '" . (int)$category_id . " ... [0m                                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          142┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "category_filter` WHERE `category_id` = '" .       
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          146┆ [1m[24m$this->db->query("INSERT INTO `" . DB_PREFIX . "category_filter` SET `category_id` = '" .         
  (int)$category_id . "', `filter_id` = '" . (int)$filter_id .  ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          150┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "category_to_store` WHERE `category_id` = '" .     
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          154┆ [1m[24m$this->db->query("INSERT INTO `" . DB_PREFIX . "category_to_store` SET `category_id` = '" .       
  (int)$category_id . "', `store_id` = '" . (int)$store_id .  ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          193┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "category_to_layout` WHERE `category_id` = '" .    
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          197┆ [1m[24m$this->db->query("INSERT INTO `" . DB_PREFIX . "category_to_layout` SET `category_id` = '" .      
  (int)$category_id . "', `store_id` = '" . (int)$store_id . ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          203┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "category` WHERE `category_id` = '" .              
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          204┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "category_description` WHERE `category_id` = '" .  
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          205┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "category_filter` WHERE `category_id` = '" .       
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          206┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "category_to_store` WHERE `category_id` = '" .     
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          207┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "category_to_layout` WHERE `category_id` = '" .    
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          208┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "product_to_category` WHERE `category_id` = '" .   
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          209┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "coupon_category` WHERE `category_id` = '" .       
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          210┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "seo_url` WHERE `key` = 'path' AND `value` = '" .  
  $this->db->escape($this->getPath($category_id)) . "'") ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          211┆ [1m[24m$this->db->query("DELETE FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '" .         
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          213┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `path_id` = '" .  
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          221┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category` WHERE `parent_id` = '" .     
  (int)$parent_id . "'");[0m                                                                                            
            ⋮┆----------------------------------------
          230┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '"
  . (int)$parent_id . "' ORDER BY `level` ASC");[0m                                                                     
            ⋮┆----------------------------------------
          245┆ [1m[24m$query = $this->db->query("SELECT DISTINCT *, (SELECT GROUP_CONCAT(cd1.`name` ORDER BY `level`    
  SEPARATOR ' > ') FROM `" . DB_PREFIX . "category_path` c ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          255┆ [1m[24m$query = $this->db->query("SELECT `category_id`, `path_id`, `level` FROM `" . DB_PREFIX .         
  "category_path` WHERE `category_id` = '" . (int)$category_id  ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          306┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_description` WHERE            
  `category_id` = '" . (int)$category_id . "'");[0m                                                                     
            ⋮┆----------------------------------------
          324┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_filter` WHERE `category_id` = 
  '" . (int)$category_id . "'");[0m                                                                                     
            ⋮┆----------------------------------------
          336┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE `key` = 'path' AND      
  `value` = '" . $this->db->escape($this->getPath($category_ ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          348┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_to_store` WHERE `category_id` 
  = '" . (int)$category_id . "'");[0m                                                                                   
            ⋮┆----------------------------------------
          360┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_to_layout` WHERE `category_id`
  = '" . (int)$category_id . "'");[0m                                                                                   
            ⋮┆----------------------------------------
          376┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "category_to_layout`  
  WHERE `layout_id` = '" . (int)$layout_id . "'");[0m                                                                   
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           20┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '"
  . (int)$data['parent_id'] . "' ORDER BY `level` ASC" ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           92┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `path_id` = '" .  
  (int)$category_id . "' ORDER BY `level` ASC");[0m                                                                     
            ⋮┆----------------------------------------
          102┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '"
  . (int)$data['parent_id'] . "' ORDER BY `level` ASC" ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          109┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '"
  . (int)$category_path['category_id'] . "' ORDER BY ` ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          131┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '"
  . (int)$data['parent_id'] . "' ORDER BY `level` ASC" ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          213┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `path_id` = '" .  
  (int)$category_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
          221┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category` WHERE `parent_id` = '" .     
  (int)$parent_id . "'");[0m                                                                                            
            ⋮┆----------------------------------------
          230┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '"
  . (int)$parent_id . "' ORDER BY `level` ASC");[0m                                                                     
            ⋮┆----------------------------------------
          245┆ [1m[24m$query = $this->db->query("SELECT DISTINCT *, (SELECT GROUP_CONCAT(cd1.`name` ORDER BY `level`    
  SEPARATOR ' > ') FROM `" . DB_PREFIX . "category_path` c ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          255┆ [1m[24m$query = $this->db->query("SELECT `category_id`, `path_id`, `level` FROM `" . DB_PREFIX .         
  "category_path` WHERE `category_id` = '" . (int)$category_id  ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          261┆ [1m[24m$sql = "SELECT cp.`category_id` AS `category_id`, GROUP_CONCAT(cd1.`name` ORDER BY cp.`level`     
  SEPARATOR ' > ') AS `name`, c1.`parent_id`, c1.`sort_orde ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          306┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_description` WHERE            
  `category_id` = '" . (int)$category_id . "'");[0m                                                                     
            ⋮┆----------------------------------------
          324┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_filter` WHERE `category_id` = 
  '" . (int)$category_id . "'");[0m                                                                                     
            ⋮┆----------------------------------------
          336┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE `key` = 'path' AND      
  `value` = '" . $this->db->escape($this->getPath($category_ ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          348┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_to_store` WHERE `category_id` 
  = '" . (int)$category_id . "'");[0m                                                                                   
            ⋮┆----------------------------------------
          360┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_to_layout` WHERE `category_id`
  = '" . (int)$category_id . "'");[0m                                                                                   
            ⋮┆----------------------------------------
          370┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "category`");[0m
            ⋮┆----------------------------------------
          376┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "category_to_layout`  
  WHERE `layout_id` = '" . (int)$layout_id . "'");[0m                                                                   
                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/catalog/download.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           32┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "download` d LEFT JOIN `" .    
  DB_PREFIX . "download_description` dd ON (d.`download_id ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           81┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "download_description` WHERE            
  `download_id` = '" . (int)$download_id . "'");[0m                                                                     
            ⋮┆----------------------------------------
          105┆ [1m[24m$query = $this->db->query("SELECT `ip`, `store_id`, `country`, `date_added` FROM `" . DB_PREFIX . 
  "download_report` WHERE `download_id` = '" . (int)$do ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          111┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "download_report`     
  WHERE `download_id` = '" . (int)$download_id . "'");[0m                                                               
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           32┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "download` d LEFT JOIN `" .    
  DB_PREFIX . "download_description` dd ON (d.`download_id ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           38┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "download` d LEFT JOIN `" . DB_PREFIX .                    
  "download_description` dd ON (d.`download_id` = dd.`download_id`) WHERE  ... [0m                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           81┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "download_description` WHERE            
  `download_id` = '" . (int)$download_id . "'");[0m                                                                     
            ⋮┆----------------------------------------
           91┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "download`");[0m
            ⋮┆----------------------------------------
          105┆ [1m[24m$query = $this->db->query("SELECT `ip`, `store_id`, `country`, `date_added` FROM `" . DB_PREFIX . 
  "download_report` WHERE `download_id` = '" . (int)$do ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          111┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "download_report`     
  WHERE `download_id` = '" . (int)$download_id . "'");[0m                                                               
                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/catalog/filter.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           65┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "filter_group` fg LEFT JOIN `" .        
  DB_PREFIX . "filter_group_description` fgd ON (fg.`filter_gr ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          110┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "filter_group_description` WHERE        
  `filter_group_id` = '" . (int)$filter_group_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          120┆ [1m[24m$query = $this->db->query("SELECT *, (SELECT `name` FROM `" . DB_PREFIX .                         
  "filter_group_description` fgd WHERE f.`filter_group_id` = fgd.`filter_group_ ... [0m                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          154┆ [1m[24m$filter_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "filter` WHERE `filter_group_id` 
  = '" . (int)$filter_group_id . "'");[0m                                                                               
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           65┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "filter_group` fg LEFT JOIN `" .        
  DB_PREFIX . "filter_group_description` fgd ON (fg.`filter_gr ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           71┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "filter_group` fg LEFT JOIN `" . DB_PREFIX .               
  "filter_group_description` fgd ON (fg.`filter_group_id` = fgd.`filt ... [0m                                           
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          110┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "filter_group_description` WHERE        
  `filter_group_id` = '" . (int)$filter_group_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          120┆ [1m[24m$query = $this->db->query("SELECT *, (SELECT `name` FROM `" . DB_PREFIX .                         
  "filter_group_description` fgd WHERE f.`filter_group_id` = fgd.`filter_group_ ... [0m                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          126┆ [1m[24m$sql = "SELECT *, (SELECT name FROM `" . DB_PREFIX . "filter_group_description` fgd WHERE         
  f.`filter_group_id` = fgd.`filter_group_id` AND fgd.`language ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          154┆ [1m[24m$filter_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "filter` WHERE `filter_group_id` 
  = '" . (int)$filter_group_id . "'");[0m                                                                               
            ⋮┆----------------------------------------
          159┆ [1m[24m$filter_description_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "filter_description` 
  WHERE `filter_id` = '" . (int)$filter['filter_id'] .  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          176┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "filter_group`");[0m
                                                                                     
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/catalog/information.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           88┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "information` WHERE            
  `information_id` = '" . (int)$information_id . "'");[0m                                                               
            ⋮┆----------------------------------------
          141┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "information_description` WHERE         
  `information_id` = '" . (int)$information_id . "'");[0m                                                               
            ⋮┆----------------------------------------
          159┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "information_to_store` WHERE            
  `information_id` = '" . (int)$information_id . "'");[0m                                                               
            ⋮┆----------------------------------------
          171┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE `key` = 'information_id'
  AND `value` = '" . (int)$information_id . "'");[0m                                                                    
            ⋮┆----------------------------------------
          183┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "information_to_layout` WHERE           
  `information_id` = '" . (int)$information_id . "'");[0m                                                               
            ⋮┆----------------------------------------
          199┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX .                       
  "information_to_layout` WHERE `layout_id` = '" . (int)$layout_id . "'");[0 ... [0m                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           88┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "information` WHERE            
  `information_id` = '" . (int)$information_id . "'");[0m                                                               
            ⋮┆----------------------------------------
           94┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "information` i LEFT JOIN `" . DB_PREFIX .                 
  "information_description` id ON (i.`information_id` = id.`information ... [0m                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          141┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "information_description` WHERE         
  `information_id` = '" . (int)$information_id . "'");[0m                                                               
            ⋮┆----------------------------------------
          159┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "information_to_store` WHERE            
  `information_id` = '" . (int)$information_id . "'");[0m                                                               
            ⋮┆----------------------------------------
          171┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE `key` = 'information_id'
  AND `value` = '" . (int)$information_id . "'");[0m                                                                    
            ⋮┆----------------------------------------
          183┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "information_to_layout` WHERE           
  `information_id` = '" . (int)$information_id . "'");[0m                                                               
            ⋮┆----------------------------------------
          193┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "information`");[0m
            ⋮┆----------------------------------------
          199┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX .                       
  "information_to_layout` WHERE `layout_id` = '" . (int)$layout_id . "'");[0 ... [0m                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                      
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/catalog/manufacturer.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           85┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "manufacturer` WHERE           
  `manufacturer_id` = '" . (int)$manufacturer_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          134┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "manufacturer_to_store` WHERE           
  `manufacturer_id` = '" . (int)$manufacturer_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          146┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE `key` =                 
  'manufacturer_id' AND `value` = '" . (int)$manufacturer_id . "'");[0 ... [0m                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          158┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "manufacturer_to_layout` WHERE          
  `manufacturer_id` = '" . (int)$manufacturer_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          174┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX .                       
  "manufacturer_to_layout` WHERE `layout_id` = '" . (int)$layout_id . "'");[ ... [0m                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           85┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "manufacturer` WHERE           
  `manufacturer_id` = '" . (int)$manufacturer_id . "'");[0m                                                             
            ⋮┆----------------------------------------
           91┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "manufacturer`";[0m
            ⋮┆----------------------------------------
          134┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "manufacturer_to_store` WHERE           
  `manufacturer_id` = '" . (int)$manufacturer_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          146┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE `key` =                 
  'manufacturer_id' AND `value` = '" . (int)$manufacturer_id . "'");[0 ... [0m                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          158┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "manufacturer_to_layout` WHERE          
  `manufacturer_id` = '" . (int)$manufacturer_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          168┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "manufacturer`");[0m
            ⋮┆----------------------------------------
          174┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX .                       
  "manufacturer_to_layout` WHERE `layout_id` = '" . (int)$layout_id . "'");[ ... [0m                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/catalog/option.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           65┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "option` o LEFT JOIN `" . DB_PREFIX .   
  "option_description` od ON (o.`option_id` = od.`option_ ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          115┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "option_description` WHERE `option_id` =
  '" . (int)$option_id . "'");[0m                                                                                       
            ⋮┆----------------------------------------
          125┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "option_value` ov LEFT JOIN `" .        
  DB_PREFIX . "option_value_description` ovd ON (ov.`option_va ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          133┆ [1m[24m$option_value_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "option_value` ov LEFT JOIN
  `" . DB_PREFIX . "option_value_description` ovd ON ( ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          150┆ [1m[24m$option_value_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "option_value` WHERE       
  `option_id` = '" . (int)$option_id . "' ORDER BY `sort_orde ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           65┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "option` o LEFT JOIN `" . DB_PREFIX .   
  "option_description` od ON (o.`option_id` = od.`option_ ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           71┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "option` o LEFT JOIN `" . DB_PREFIX . "option_description` 
  od ON (o.`option_id` = od.`option_id`) WHERE od.`lang ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          115┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "option_description` WHERE `option_id` =
  '" . (int)$option_id . "'");[0m                                                                                       
            ⋮┆----------------------------------------
          125┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "option_value` ov LEFT JOIN `" .        
  DB_PREFIX . "option_value_description` ovd ON (ov.`option_va ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          133┆ [1m[24m$option_value_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "option_value` ov LEFT JOIN
  `" . DB_PREFIX . "option_value_description` ovd ON ( ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          150┆ [1m[24m$option_value_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "option_value` WHERE       
  `option_id` = '" . (int)$option_id . "' ORDER BY `sort_orde ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          155┆ [1m[24m$option_value_description_query = $this->db->query("SELECT * FROM `" . DB_PREFIX .                
  "option_value_description` WHERE `option_value_id` = '" . (int)$opti ... [0m                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          173┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "option`");[0m
                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/catalog/review.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           46┆ [1m[24m$query = $this->db->query("SELECT DISTINCT *, (SELECT pd.`name` FROM `" . DB_PREFIX .             
  "product_description` pd WHERE pd.`product_id` = r.`product_id` A ... [0m                                             
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           52┆ [1m[24m$query = $this->db->query("SELECT AVG(`rating`) AS `total` FROM `" . DB_PREFIX . "review` WHERE   
  `product_id` = '" . (int)$product_id . "' AND `status`  ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           46┆ [1m[24m$query = $this->db->query("SELECT DISTINCT *, (SELECT pd.`name` FROM `" . DB_PREFIX .             
  "product_description` pd WHERE pd.`product_id` = r.`product_id` A ... [0m                                             
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           52┆ [1m[24m$query = $this->db->query("SELECT AVG(`rating`) AS `total` FROM `" . DB_PREFIX . "review` WHERE   
  `product_id` = '" . (int)$product_id . "' AND `status`  ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           62┆ [1m[24m$sql = "SELECT r.`review_id`, pd.`name`, r.`author`, r.`rating`, r.`status`, r.`date_added` FROM  
  `" . DB_PREFIX . "review` r LEFT JOIN `" . DB_PREFIX . ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          122┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "review` r LEFT JOIN `" . DB_PREFIX .    
  "product_description` pd ON (r.`product_id` = pd.`produc ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          150┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "review` WHERE        
  `status` = '0'");[0m                                                                                                  
                                                                                       
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/customer/custom_field.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           84┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field` cf LEFT JOIN `" .        
  DB_PREFIX . "custom_field_description` cfd ON (cf.`custom_fi ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          152┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field_description` WHERE        
  `custom_field_id` = '" . (int)$custom_field_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          162┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field_value` cfv LEFT JOIN `" . 
  DB_PREFIX . "custom_field_value_description` cfvd ON  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          170┆ [1m[24m$custom_field_value_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field_value` 
  cfv LEFT JOIN `" . DB_PREFIX . "custom_field_value_de ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          183┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field_customer_group` WHERE     
  `custom_field_id` = '" . (int)$custom_field_id . "'");[0 ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          191┆ [1m[24m$custom_field_value_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field_value` 
  WHERE `custom_field_id` = '" . (int)$custom_field_id  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           84┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field` cf LEFT JOIN `" .        
  DB_PREFIX . "custom_field_description` cfd ON (cf.`custom_fi ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           91┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "custom_field` cf LEFT JOIN `" . DB_PREFIX .               
  "custom_field_description` cfd ON (cf.`custom_field_id` = cfd.`cust ... [0m                                           
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           93┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "custom_field_customer_group` cfcg LEFT JOIN `" . DB_PREFIX
  . "custom_field` cf ON (cfcg.`custom_field_id` = cf. ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          152┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field_description` WHERE        
  `custom_field_id` = '" . (int)$custom_field_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          162┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field_value` cfv LEFT JOIN `" . 
  DB_PREFIX . "custom_field_value_description` cfvd ON  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          170┆ [1m[24m$custom_field_value_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field_value` 
  cfv LEFT JOIN `" . DB_PREFIX . "custom_field_value_de ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          183┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field_customer_group` WHERE     
  `custom_field_id` = '" . (int)$custom_field_id . "'");[0 ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          191┆ [1m[24m$custom_field_value_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field_value` 
  WHERE `custom_field_id` = '" . (int)$custom_field_id  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          196┆ [1m[24m$custom_field_value_description_query = $this->db->query("SELECT * FROM `" . DB_PREFIX .          
  "custom_field_value_description` WHERE `custom_field_value_id` ... [0m                                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          213┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "custom_field`");[0m
                                                                                            
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/customer/customer_approval.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           51┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "customer_approval` WHERE               
  `customer_approval_id` = '" . (int)$customer_approval_id . "'");[0 ... [0m                                            
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$sql = "SELECT *, CONCAT(c.`firstname`, ' ', c.`lastname`) AS customer, cgd.`name` AS             
  customer_group, ca.`type` FROM `" . DB_PREFIX . "customer_approva ... [0m                                             
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           51┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "customer_approval` WHERE               
  `customer_approval_id` = '" . (int)$customer_approval_id . "'");[0 ... [0m                                            
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           57┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "customer_approval` ca LEFT JOIN `" .    
  DB_PREFIX . "customer` c ON (ca.`customer_id` = c.`custo ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                         
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/customer/customer_group.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           36┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "customer_group` cg LEFT JOIN  
  `" . DB_PREFIX . "customer_group_description` cgd ON ( ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           81┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "customer_group_description` WHERE      
  `customer_group_id` = '" . (int)$customer_group_id . "'"); ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           36┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "customer_group` cg LEFT JOIN  
  `" . DB_PREFIX . "customer_group_description` cgd ON ( ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           42┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "customer_group` cg LEFT JOIN `" . DB_PREFIX .             
  "customer_group_description` cgd ON (cg.`customer_group_id` = cgd ... [0m                                             
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           81┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "customer_group_description` WHERE      
  `customer_group_id` = '" . (int)$customer_group_id . "'"); ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           94┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "customer_group`");[0m
                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/customer/gdpr.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           61┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "gdpr` WHERE `gdpr_id` = '" .           
  (int)$gdpr_id . "'");[0m                                                                                              
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           13┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "gdpr`";[0m
            ⋮┆----------------------------------------
           61┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "gdpr` WHERE `gdpr_id` = '" .           
  (int)$gdpr_id . "'");[0m                                                                                              
            ⋮┆----------------------------------------
           67┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "gdpr`";[0m
            ⋮┆----------------------------------------
          101┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "gdpr` WHERE `status` = '2' AND         
  DATE(`date_added`) <= DATE('" . $this->db->escape(date('Y-m-d ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/design/banner.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           40┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "banner` WHERE `banner_id` = '"
  . (int)$banner_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
           85┆ [1m[24m$banner_image_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "banner_image` WHERE       
  `banner_id` = '" . (int)$banner_id . "' ORDER BY `sort_orde ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           40┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "banner` WHERE `banner_id` = '"
  . (int)$banner_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
           46┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "banner`";[0m
            ⋮┆----------------------------------------
           85┆ [1m[24m$banner_image_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "banner_image` WHERE       
  `banner_id` = '" . (int)$banner_id . "' ORDER BY `sort_orde ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          100┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "banner`");[0m
                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/design/layout.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           54┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "layout` WHERE `layout_id` = '"
  . (int)$layout_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
           94┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "layout_route` WHERE `layout_id` = '" . 
  (int)$layout_id . "'");[0m                                                                                            
            ⋮┆----------------------------------------
          100┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "layout_module` WHERE `layout_id` = '" .
  (int)$layout_id . "' ORDER BY `position` ASC, `sort_ ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           54┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "layout` WHERE `layout_id` = '"
  . (int)$layout_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
           60┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "layout`";[0m
            ⋮┆----------------------------------------
           94┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "layout_route` WHERE `layout_id` = '" . 
  (int)$layout_id . "'");[0m                                                                                            
            ⋮┆----------------------------------------
          100┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "layout_module` WHERE `layout_id` = '" .
  (int)$layout_id . "' ORDER BY `position` ASC, `sort_ ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          106┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "layout`");[0m
                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/design/seo_url.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           19┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE `seo_url_id` = '" .     
  (int)$seo_url_id . "'");[0m                                                                                           
            ⋮┆----------------------------------------
          125┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE `key` = '" .            
  $this->db->escape($key) . "' AND `value` = '" . $this->db->escap ... [0m                                              
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          131┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE (`keyword` = '" .                          
  $this->db->escape($keyword) . "' OR `keyword` LIKE '" . $this->db->escape('%/' ... [0m                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           19┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE `seo_url_id` = '" .     
  (int)$seo_url_id . "'");[0m                                                                                           
            ⋮┆----------------------------------------
           25┆ [1m[24m$sql = "SELECT *, (SELECT `name` FROM `" . DB_PREFIX . "store` s WHERE s.`store_id` =             
  su.`store_id`) AS `store`, (SELECT `name` FROM `" . DB_PREFIX . " ... [0m                                             
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           91┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "seo_url`";[0m
            ⋮┆----------------------------------------
          125┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE `key` = '" .            
  $this->db->escape($key) . "' AND `value` = '" . $this->db->escap ... [0m                                              
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          131┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE (`keyword` = '" .                          
  $this->db->escape($keyword) . "' OR `keyword` LIKE '" . $this->db->escape('%/' ... [0m                                
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                              
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/design/theme.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           15┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "theme` WHERE `store_id` = '" .         
  (int)$store_id . "' AND `route` = '" . $this->db->escape($rou ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           29┆ [1m[24m$query = $this->db->query("SELECT *, (SELECT `name` FROM `" . DB_PREFIX . "store` s WHERE         
  s.`store_id` = t.`store_id`) AS `store` FROM `" . DB_PREFIX . ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           15┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "theme` WHERE `store_id` = '" .         
  (int)$store_id . "' AND `route` = '" . $this->db->escape($rou ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           29┆ [1m[24m$query = $this->db->query("SELECT *, (SELECT `name` FROM `" . DB_PREFIX . "store` s WHERE         
  s.`store_id` = t.`store_id`) AS `store` FROM `" . DB_PREFIX . ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           35┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "theme`");[0m
                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/design/translation.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           17┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "translation` WHERE            
  `translation_id` = '" . (int)$translation_id . "'");[0m                                                               
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           17┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "translation` WHERE            
  `translation_id` = '" . (int)$translation_id . "'");[0m                                                               
            ⋮┆----------------------------------------
           23┆ [1m[24m$sql = "SELECT *, (SELECT s.`name` FROM `" . DB_PREFIX . "store` s WHERE s.`store_id` =           
  t.`store_id`) AS store, (SELECT l.`name` FROM `" . DB_PREFIX .  ... [0m                                               
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           63┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "translation`");[0m
                                                                                             
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/address_format.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           19┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "address_format` WHERE         
  `address_format_id` = '" . (int)$address_format_id . "'");[0 ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           19┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "address_format` WHERE         
  `address_format_id` = '" . (int)$address_format_id . "'");[0 ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           25┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "address_format`";[0m
            ⋮┆----------------------------------------
           45┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "address_format`");[0m
                                                                                      
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/country.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           25┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "country` WHERE `country_id` = 
  '" . (int)$country_id . "'");[0m                                                                                      
            ⋮┆----------------------------------------
           31┆ [1m[24m$query = $this->db->query("SELECT * FROM " . DB_PREFIX . "country WHERE `iso_code_2` = '" .       
  $this->db->escape($iso_code_2) . "' AND `status` = '1'");[ ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM " . DB_PREFIX . "country WHERE `iso_code_3` = '" .       
  $this->db->escape($iso_code_3) . "' AND `status` = '1'");[ ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          133┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "country` WHERE       
  `address_format_id` = '" . (int)$address_format_id . "'"); ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           25┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "country` WHERE `country_id` = 
  '" . (int)$country_id . "'");[0m                                                                                      
            ⋮┆----------------------------------------
           31┆ [1m[24m$query = $this->db->query("SELECT * FROM " . DB_PREFIX . "country WHERE `iso_code_2` = '" .       
  $this->db->escape($iso_code_2) . "' AND `status` = '1'");[ ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM " . DB_PREFIX . "country WHERE `iso_code_3` = '" .       
  $this->db->escape($iso_code_3) . "' AND `status` = '1'");[ ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           43┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "country`";[0m
            ⋮┆----------------------------------------
          107┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "country`";[0m
            ⋮┆----------------------------------------
          133┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "country` WHERE       
  `address_format_id` = '" . (int)$address_format_id . "'"); ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                       
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/currency.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           31┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "currency` WHERE `currency_id` 
  = '" . (int)$currency_id . "'");[0m                                                                                   
            ⋮┆----------------------------------------
           37┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "currency` WHERE `code` = '" . 
  $this->db->escape($currency) . "'");[0m                                                                               
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           31┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "currency` WHERE `currency_id` 
  = '" . (int)$currency_id . "'");[0m                                                                                   
            ⋮┆----------------------------------------
           37┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "currency` WHERE `code` = '" . 
  $this->db->escape($currency) . "'");[0m                                                                               
            ⋮┆----------------------------------------
           43┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "currency`";[0m
            ⋮┆----------------------------------------
          106┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "currency`");[0m
                                                                                       
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/geo_zone.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           46┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "geo_zone` WHERE `geo_zone_id` 
  = '" . (int)$geo_zone_id . "'");[0m                                                                                   
            ⋮┆----------------------------------------
          103┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$geo_zone_id . "'");[0m                                                                                     
            ⋮┆----------------------------------------
          109┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "zone_to_geo_zone`    
  WHERE `geo_zone_id` = '" . (int)$geo_zone_id . "'");[0m                                                               
            ⋮┆----------------------------------------
          115┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "zone_to_geo_zone`    
  WHERE `country_id` = '" . (int)$country_id . "'");[0m                                                                 
            ⋮┆----------------------------------------
          121┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "zone_to_geo_zone`    
  WHERE `zone_id` = '" . (int)$zone_id . "'");[0m                                                                       
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           46┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "geo_zone` WHERE `geo_zone_id` 
  = '" . (int)$geo_zone_id . "'");[0m                                                                                   
            ⋮┆----------------------------------------
           52┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "geo_zone`";[0m
            ⋮┆----------------------------------------
           97┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "geo_zone`");[0m
            ⋮┆----------------------------------------
          103┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$geo_zone_id . "'");[0m                                                                                     
            ⋮┆----------------------------------------
          109┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "zone_to_geo_zone`    
  WHERE `geo_zone_id` = '" . (int)$geo_zone_id . "'");[0m                                                               
            ⋮┆----------------------------------------
          115┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "zone_to_geo_zone`    
  WHERE `country_id` = '" . (int)$country_id . "'");[0m                                                                 
            ⋮┆----------------------------------------
          121┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "zone_to_geo_zone`    
  WHERE `zone_id` = '" . (int)$zone_id . "'");[0m                                                                       
                                                                                       
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/language.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$this->db->query("INSERT INTO `" . DB_PREFIX . "language` SET `name` = '" .                       
  $this->db->escape((string)$data['name']) . "', `code` = '" . $this->db->esc ... [0m                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          222┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "language` WHERE `language_id` 
  = '" . (int)$language_id . "'");[0m                                                                                   
            ⋮┆----------------------------------------
          242┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "language` WHERE `code` = '" .          
  $this->db->escape($code) . "'");[0m                                                                                   
                                                                                           
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/length_class.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           84┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "length_class` lc LEFT JOIN `" .        
  DB_PREFIX . "length_class_description` lcd ON (lc.`length_cl ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           90┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "length_class_description` WHERE `unit` 
  = '" . $this->db->escape($unit) . "' AND `language_id ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           98┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "length_class_description` WHERE        
  `length_class_id` = '" . (int)$length_class_id . "'");[0m                                                             
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           38┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "length_class` lc LEFT JOIN `" . DB_PREFIX .               
  "length_class_description` lcd ON (lc.`length_class_id` = lcd.`leng ... [0m                                           
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           84┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "length_class` lc LEFT JOIN `" .        
  DB_PREFIX . "length_class_description` lcd ON (lc.`length_cl ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           90┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "length_class_description` WHERE `unit` 
  = '" . $this->db->escape($unit) . "' AND `language_id ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           98┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "length_class_description` WHERE        
  `length_class_id` = '" . (int)$length_class_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          111┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "length_class`");[0m
                                                                                       
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/location.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           19┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "location` WHERE `location_id` 
  = '" . (int)$location_id . "'");[0m                                                                                   
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           19┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "location` WHERE `location_id` 
  = '" . (int)$location_id . "'");[0m                                                                                   
            ⋮┆----------------------------------------
           25┆ [1m[24m$sql = "SELECT `location_id`, `name`, `address` FROM `" . DB_PREFIX . "location`";[0m
            ⋮┆----------------------------------------
           62┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "location`");[0m
                                                                                           
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/order_status.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_status` WHERE `order_status_id` =
  '" . (int)$order_status_id . "' AND `language_id` =  ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_status` WHERE `order_status_id` =
  '" . (int)$order_status_id . "'");[0m                                                                                 
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_status` WHERE `order_status_id` =
  '" . (int)$order_status_id . "' AND `language_id` =  ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           43┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "order_status` WHERE `language_id` = '" .                  
  (int)$this->config->get('config_language_id') . "' ORDER BY `name`";[ ... [0m                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_status` WHERE `order_status_id` =
  '" . (int)$order_status_id . "'");[0m                                                                                 
            ⋮┆----------------------------------------
           89┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_status` WHERE  
  `language_id` = '" . (int)$this->config->get('config_l ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                            
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/return_action.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "return_action` WHERE `return_action_id`
  = '" . (int)$return_action_id . "' AND `language_id` ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "return_action` WHERE `return_action_id`
  = '" . (int)$return_action_id . "'");[0m                                                                              
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "return_action` WHERE `return_action_id`
  = '" . (int)$return_action_id . "' AND `language_id` ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           43┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "return_action` WHERE `language_id` = '" .                 
  (int)$this->config->get('config_language_id') . "' ORDER BY `name`"; ... [0m                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "return_action` WHERE `return_action_id`
  = '" . (int)$return_action_id . "'");[0m                                                                              
            ⋮┆----------------------------------------
           89┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "return_action` WHERE 
  `language_id` = '" . (int)$this->config->get('config_ ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                            
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/return_reason.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "return_reason` WHERE `return_reason_id`
  = '" . (int)$return_reason_id . "' AND `language_id` ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "return_reason` WHERE `return_reason_id`
  = '" . (int)$return_reason_id . "'");[0m                                                                              
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "return_reason` WHERE `return_reason_id`
  = '" . (int)$return_reason_id . "' AND `language_id` ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           43┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "return_reason` WHERE `language_id` = '" .                 
  (int)$this->config->get('config_language_id') . "' ORDER BY `name`"; ... [0m                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "return_reason` WHERE `return_reason_id`
  = '" . (int)$return_reason_id . "'");[0m                                                                              
            ⋮┆----------------------------------------
           89┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "return_reason` WHERE 
  `language_id` = '" . (int)$this->config->get('config_ ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                            
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/return_status.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "return_status` WHERE `return_status_id`
  = '" . (int)$return_status_id . "' AND `language_id` ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "return_status` WHERE `return_status_id`
  = '" . (int)$return_status_id . "'");[0m                                                                              
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "return_status` WHERE `return_status_id`
  = '" . (int)$return_status_id . "' AND `language_id` ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           43┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "return_status` WHERE `language_id` = '" .                 
  (int)$this->config->get('config_language_id') . "' ORDER BY `name`"; ... [0m                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "return_status` WHERE `return_status_id`
  = '" . (int)$return_status_id . "'");[0m                                                                              
            ⋮┆----------------------------------------
           89┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "return_status` WHERE 
  `language_id` = '" . (int)$this->config->get('config_ ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                           
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/stock_status.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "stock_status` WHERE `stock_status_id` =
  '" . (int)$stock_status_id . "' AND `language_id` =  ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "stock_status` WHERE `stock_status_id` =
  '" . (int)$stock_status_id . "'");[0m                                                                                 
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "stock_status` WHERE `stock_status_id` =
  '" . (int)$stock_status_id . "' AND `language_id` =  ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           43┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "stock_status` WHERE `language_id` = '" .                  
  (int)$this->config->get('config_language_id') . "' ORDER BY `name`";[ ... [0m                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "stock_status` WHERE `stock_status_id` =
  '" . (int)$stock_status_id . "'");[0m                                                                                 
            ⋮┆----------------------------------------
           89┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "stock_status` WHERE  
  `language_id` = '" . (int)$this->config->get('config_l ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/subscription_status.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription_status` WHERE             
  `subscription_status_id` = '" . (int)$subscription_status_id . "' ... [0m                                             
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription_status` WHERE             
  `subscription_status_id` = '" . (int)$subscription_status_id . "' ... [0m                                             
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription_status` WHERE             
  `subscription_status_id` = '" . (int)$subscription_status_id . "' ... [0m                                             
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           43┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "subscription_status` WHERE `language_id` = '" .           
  (int)$this->config->get('config_language_id') . "' ORDER BY `na ... [0m                                               
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription_status` WHERE             
  `subscription_status_id` = '" . (int)$subscription_status_id . "' ... [0m                                             
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           89┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription_status` 
  WHERE `language_id` = '" . (int)$this->config->get('c ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                        
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/tax_class.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           42┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "tax_class` WHERE `tax_class_id` = '" . 
  (int)$tax_class_id . "'");[0m                                                                                         
            ⋮┆----------------------------------------
           88┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "tax_rule` WHERE `tax_class_id` = '" .  
  (int)$tax_class_id . "' ORDER BY `priority` ASC");[0m                                                                 
            ⋮┆----------------------------------------
           94┆ [1m[24m$query = $this->db->query("SELECT COUNT(DISTINCT `tax_class_id`) AS `total` FROM `" . DB_PREFIX . 
  "tax_rule` WHERE `tax_rate_id` = '" . (int)$tax_rate_ ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           42┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "tax_class` WHERE `tax_class_id` = '" . 
  (int)$tax_class_id . "'");[0m                                                                                         
            ⋮┆----------------------------------------
           48┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "tax_class` ORDER BY `title`";[0m
            ⋮┆----------------------------------------
           82┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "tax_class`");[0m
            ⋮┆----------------------------------------
           88┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "tax_rule` WHERE `tax_class_id` = '" .  
  (int)$tax_class_id . "' ORDER BY `priority` ASC");[0m                                                                 
            ⋮┆----------------------------------------
           94┆ [1m[24m$query = $this->db->query("SELECT COUNT(DISTINCT `tax_class_id`) AS `total` FROM `" . DB_PREFIX . 
  "tax_rule` WHERE `tax_rate_id` = '" . (int)$tax_rate_ ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                       
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/tax_rate.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           36┆ [1m[24m$query = $this->db->query("SELECT tr.`tax_rate_id`, tr.`name` AS name, tr.`rate`, tr.`type`,      
  tr.`geo_zone_id`, gz.`name` AS geo_zone, tr.`date_added`,  ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           85┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "tax_rate_to_customer_group` WHERE      
  `tax_rate_id` = '" . (int)$tax_rate_id . "'");[0m                                                                     
            ⋮┆----------------------------------------
          101┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "tax_rate` WHERE      
  `geo_zone_id` = '" . (int)$geo_zone_id . "'");[0m                                                                     
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           36┆ [1m[24m$query = $this->db->query("SELECT tr.`tax_rate_id`, tr.`name` AS name, tr.`rate`, tr.`type`,      
  tr.`geo_zone_id`, gz.`name` AS geo_zone, tr.`date_added`,  ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           42┆ [1m[24m$sql = "SELECT tr.`tax_rate_id`, tr.`name` AS name, tr.`rate`, tr.`type`, gz.`name` AS geo_zone,  
  tr.`date_added`, tr.`date_modified` FROM `" . DB_PREFI ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           85┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "tax_rate_to_customer_group` WHERE      
  `tax_rate_id` = '" . (int)$tax_rate_id . "'");[0m                                                                     
            ⋮┆----------------------------------------
           95┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "tax_rate`");[0m
            ⋮┆----------------------------------------
          101┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "tax_rate` WHERE      
  `geo_zone_id` = '" . (int)$geo_zone_id . "'");[0m                                                                     
                                                                                           
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/weight_class.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           84┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "weight_class` wc LEFT JOIN `" .        
  DB_PREFIX . "weight_class_description` wcd ON (wc.`weight_cl ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           90┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "weight_class_description` WHERE `unit` 
  = '" . $this->db->escape($unit) . "' AND `language_id ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           98┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "weight_class_description` WHERE        
  `weight_class_id` = '" . (int)$weight_class_id . "'");[0m                                                             
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           38┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "weight_class` wc LEFT JOIN `" . DB_PREFIX .               
  "weight_class_description` wcd ON (wc.`weight_class_id` = wcd.`weig ... [0m                                           
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           84┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "weight_class` wc LEFT JOIN `" .        
  DB_PREFIX . "weight_class_description` wcd ON (wc.`weight_cl ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           90┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "weight_class_description` WHERE `unit` 
  = '" . $this->db->escape($unit) . "' AND `language_id ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           98┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "weight_class_description` WHERE        
  `weight_class_id` = '" . (int)$weight_class_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          111┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "weight_class`");[0m
                                                                                   
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/localisation/zone.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           25┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "zone` WHERE `zone_id` = '" .  
  (int)$zone_id . "'");[0m                                                                                              
            ⋮┆----------------------------------------
           87┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "zone` WHERE `country_id` = '" . (int)$country_id . "' AND 
  `status` = '1' ORDER BY `name`";[0m                                                                                   
            ⋮┆----------------------------------------
          133┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "zone` WHERE          
  `country_id` = '" . (int)$country_id . "'");[0m                                                                       
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           25┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "zone` WHERE `zone_id` = '" .  
  (int)$zone_id . "'");[0m                                                                                              
            ⋮┆----------------------------------------
           31┆ [1m[24m$sql = "SELECT *, z.`name`, c.`name` AS country FROM `" . DB_PREFIX . "zone` z LEFT JOIN `" .     
  DB_PREFIX . "country` c ON (z.`country_id` = c.`country_i ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           87┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "zone` WHERE `country_id` = '" . (int)$country_id . "' AND 
  `status` = '1' ORDER BY `name`";[0m                                                                                   
            ⋮┆----------------------------------------
          103┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "zone` z";[0m
            ⋮┆----------------------------------------
          133┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "zone` WHERE          
  `country_id` = '" . (int)$country_id . "'");[0m                                                                       
                                                                                     
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/marketing/marketing.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           19┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "marketing` WHERE              
  `marketing_id` = '" . (int)$marketing_id . "'");[0m                                                                   
            ⋮┆----------------------------------------
           25┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "marketing` WHERE `code` = '" .
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
          137┆ [1m[24m$query = $this->db->query("SELECT `ip`, `store_id`, `country`, `date_added` FROM `" . DB_PREFIX . 
  "marketing_report` WHERE `marketing_id` = '" . (int)$ ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          143┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "marketing_report`    
  WHERE `marketing_id` = '" . (int)$marketing_id . "'");[ ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           19┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "marketing` WHERE              
  `marketing_id` = '" . (int)$marketing_id . "'");[0m                                                                   
            ⋮┆----------------------------------------
           25┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "marketing` WHERE `code` = '" .
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
           39┆ [1m[24m$sql = "SELECT *, (SELECT COUNT(*) FROM `" . DB_PREFIX . "order` o WHERE (" . implode(" OR ",     
  $implode) . ") AND o.`marketing_id` = m.`marketing_id`) A ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           99┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "marketing`";[0m
            ⋮┆----------------------------------------
          137┆ [1m[24m$query = $this->db->query("SELECT `ip`, `store_id`, `country`, `date_added` FROM `" . DB_PREFIX . 
  "marketing_report` WHERE `marketing_id` = '" . (int)$ ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          143┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "marketing_report`    
  WHERE `marketing_id` = '" . (int)$marketing_id . "'");[ ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/report/online.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$sql = "SELECT co.`ip`, co.`customer_id`, co.`url`, co.`referer`, co.`date_added` FROM `" .       
  DB_PREFIX . "customer_online` co LEFT JOIN `" . DB_PREFIX . ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           41┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "customer_online` co LEFT JOIN `" .      
  DB_PREFIX . "customer` c ON (co.`customer_id` = c.`custome ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                   
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/report/statistics.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           11┆ [1m[24m$query = $this->db->query("SELECT `value` FROM `" . DB_PREFIX . "statistics` WHERE `code` = '" .  
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "statistics`");[0m
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT `value` FROM `" . DB_PREFIX . "statistics` WHERE `code` = '" .  
  $this->db->escape($code) . "'");[0m                                                                                   
                                                                            
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/sale/order.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$order_query = $this->db->query("SELECT *, (SELECT `os`.`name` FROM `" . DB_PREFIX .              
  "order_status` os WHERE `os`.`order_status_id` = `o`.`order_status ... [0m                                            
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           46┆ [1m[24m$order_product_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_product` WHERE     
  `order_id` = '" . (int)$order_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
          240┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order` WHERE `subscription_id` = '" .  
  (int)$subscription_id . "'");[0m                                                                                      
            ⋮┆----------------------------------------
          246┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE         
  `subscription_id` = '" . (int)$subscription_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          252┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_product` WHERE `order_id` = '" . 
  (int)$order_id . "' ORDER BY order_product_id ASC"); ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          258┆ [1m[24m$sql = "SELECT SUM(op.quantity) AS `total` FROM `" . DB_PREFIX . "order_product` `op` LEFT JOIN `"
  . DB_PREFIX . "order` `o` ON (`op`.`order_id` = `o`. ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          284┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_option` WHERE `order_id` = '" .  
  (int)$order_id . "' AND `order_product_id` = '" . (int ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          290┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_subscription` WHERE `order_id` = 
  '" . (int)$order_id . "' AND `order_product_id` = '"  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          296┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_voucher` WHERE `order_id` = '" . 
  (int)$order_id . "'");[0m                                                                                             
            ⋮┆----------------------------------------
          302┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_voucher` WHERE `voucher_id` = '" 
  . (int)$voucher_id . "'");[0m                                                                                         
            ⋮┆----------------------------------------
          308┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_total` WHERE `order_id` = '" .   
  (int)$order_id . "' ORDER BY `sort_order`");[0m                                                                       
            ⋮┆----------------------------------------
          372┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE         
  `store_id` = '" . (int)$store_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
          378┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE         
  `order_status_id` = '" . (int)$order_status_id . "' AND `orde ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          420┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE         
  `language_id` = '" . (int)$language_id . "' AND `order_status ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          426┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE         
  `currency_id` = '" . (int)$currency_id . "' AND `order_status ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          501┆ [1m[24m$this->db->query("UPDATE `" . DB_PREFIX . "order` SET `invoice_no` = '" . (int)$invoice_no . "',  
  `invoice_prefix` = '" . $this->db->escape($order_info[ ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          510┆ [1m[24m$query = $this->db->query("SELECT SUM(reward) AS `total` FROM `" . DB_PREFIX . "order_product`    
  WHERE `order_id` = '" . (int)$order_id . "'");[0m                                                                     
            ⋮┆----------------------------------------
          524┆ [1m[24m$query = $this->db->query("SELECT oh.`date_added`, os.`name` AS `status`, oh.`comment`,           
  oh.`notify` FROM `" . DB_PREFIX . "order_history` oh LEFT JOIN  ... [0m                                               
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          530┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_history` WHERE 
  `order_id` = '" . (int)$order_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
          536┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_history` WHERE 
  `order_status_id` = '" . (int)$order_status_id . "'") ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          548┆ [1m[24m$query = $this->db->query("SELECT DISTINCT o.`email` FROM `" . DB_PREFIX . "order` o LEFT JOIN `" 
  . DB_PREFIX . "order_product` op ON (o.`order_id` = o ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$order_query = $this->db->query("SELECT *, (SELECT `os`.`name` FROM `" . DB_PREFIX .              
  "order_status` os WHERE `os`.`order_status_id` = `o`.`order_status ... [0m                                            
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
            8┆ [1m[24m$country_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "country` WHERE `country_id` =  
  '" . (int)$order_query->row['payment_country_id'] . "' ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           18┆ [1m[24m$zone_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone` WHERE `zone_id` = '" .      
  (int)$order_query->row['payment_zone_id'] . "'");[0m                                                                  
            ⋮┆----------------------------------------
           26┆ [1m[24m$country_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "country` WHERE `country_id` =  
  '" . (int)$order_query->row['shipping_country_id'] . " ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           36┆ [1m[24m$zone_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone` WHERE `zone_id` = '" .      
  (int)$order_query->row['shipping_zone_id'] . "'");[0m                                                                 
            ⋮┆----------------------------------------
           46┆ [1m[24m$order_product_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_product` WHERE     
  `order_id` = '" . (int)$order_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
          148┆ [1m[24m$sql = "SELECT o.`order_id`, CONCAT(o.`firstname`, ' ', o.`lastname`) AS customer, (SELECT        
  os.`name` FROM `" . DB_PREFIX . "order_status` os WHERE os.` ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          240┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order` WHERE `subscription_id` = '" .  
  (int)$subscription_id . "'");[0m                                                                                      
            ⋮┆----------------------------------------
          246┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE         
  `subscription_id` = '" . (int)$subscription_id . "'");[0m                                                             
            ⋮┆----------------------------------------
          252┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_product` WHERE `order_id` = '" . 
  (int)$order_id . "' ORDER BY order_product_id ASC"); ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          258┆ [1m[24m$sql = "SELECT SUM(op.quantity) AS `total` FROM `" . DB_PREFIX . "order_product` `op` LEFT JOIN `"
  . DB_PREFIX . "order` `o` ON (`op`.`order_id` = `o`. ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          284┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_option` WHERE `order_id` = '" .  
  (int)$order_id . "' AND `order_product_id` = '" . (int ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          290┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_subscription` WHERE `order_id` = 
  '" . (int)$order_id . "' AND `order_product_id` = '"  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          296┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_voucher` WHERE `order_id` = '" . 
  (int)$order_id . "'");[0m                                                                                             
            ⋮┆----------------------------------------
          302┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_voucher` WHERE `voucher_id` = '" 
  . (int)$voucher_id . "'");[0m                                                                                         
            ⋮┆----------------------------------------
          308┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_total` WHERE `order_id` = '" .   
  (int)$order_id . "' ORDER BY `sort_order`");[0m                                                                       
            ⋮┆----------------------------------------
          314┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order`";[0m
            ⋮┆----------------------------------------
          372┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE         
  `store_id` = '" . (int)$store_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
          378┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE         
  `order_status_id` = '" . (int)$order_status_id . "' AND `orde ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          393┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE " .     
  implode(" OR ", $implode));[0m                                                                                        
            ⋮┆----------------------------------------
          411┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE " .     
  implode(" OR ", $implode) . "");[0m                                                                                   
            ⋮┆----------------------------------------
          420┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE         
  `language_id` = '" . (int)$language_id . "' AND `order_status ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          426┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE         
  `currency_id` = '" . (int)$currency_id . "' AND `order_status ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          432┆ [1m[24m$sql = "SELECT SUM(`total`) AS `total` FROM `" . DB_PREFIX . "order`";[0m
            ⋮┆----------------------------------------
          493┆ [1m[24m$query = $this->db->query("SELECT MAX(`invoice_no`) AS invoice_no FROM `" . DB_PREFIX . "order`   
  WHERE `invoice_prefix` = '" . $this->db->escape($order_ ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          510┆ [1m[24m$query = $this->db->query("SELECT SUM(reward) AS `total` FROM `" . DB_PREFIX . "order_product`    
  WHERE `order_id` = '" . (int)$order_id . "'");[0m                                                                     
            ⋮┆----------------------------------------
          524┆ [1m[24m$query = $this->db->query("SELECT oh.`date_added`, os.`name` AS `status`, oh.`comment`,           
  oh.`notify` FROM `" . DB_PREFIX . "order_history` oh LEFT JOIN  ... [0m                                               
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          530┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_history` WHERE 
  `order_id` = '" . (int)$order_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
          536┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_history` WHERE 
  `order_status_id` = '" . (int)$order_status_id . "'") ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          548┆ [1m[24m$query = $this->db->query("SELECT DISTINCT o.`email` FROM `" . DB_PREFIX . "order` o LEFT JOIN `" 
  . DB_PREFIX . "order_product` op ON (o.`order_id` = o ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          560┆ [1m[24m$query = $this->db->query("SELECT COUNT(DISTINCT o.`email`) AS `total` FROM `" . DB_PREFIX .      
  "order` o LEFT JOIN `" . DB_PREFIX . "order_product` op ON ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                   
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/sale/subscription.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           31┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription` WHERE `subscription_id` =
  '" . (int)$subscription_id . "'");[0m                                                                                 
            ⋮┆----------------------------------------
           44┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription` WHERE `order_id` = '" .  
  (int)$order_id . "' AND `order_product_id` = '" . (int ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          167┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription` WHERE  
  `store_id` = '" . (int)$store_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
          173┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription` WHERE  
  `subscription_status_id` = '" . (int)$subscription_sta ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          193┆ [1m[24m$query = $this->db->query("SELECT sh.`date_added`, ss.`name` AS status, sh.`comment`, sh.`notify` 
  FROM `" . DB_PREFIX . "subscription_history` sh LEFT  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          199┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription_history`
  WHERE `subscription_id` = '" . (int)$subscription_id ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          205┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription_history`
  WHERE `subscription_status_id` = '" . (int)$subscrip ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           31┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription` WHERE `subscription_id` =
  '" . (int)$subscription_id . "'");[0m                                                                                 
            ⋮┆----------------------------------------
           44┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription` WHERE `order_id` = '" .  
  (int)$order_id . "' AND `order_product_id` = '" . (int ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           50┆ [1m[24m$sql = "SELECT `s`.`subscription_id`, `s`.*, CONCAT(o.`firstname`, ' ', o.`lastname`) AS customer,
  (SELECT ss.`name` FROM `" . DB_PREFIX . "subscriptio ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          129┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription` `s` LEFT JOIN `" .        
  DB_PREFIX . "order` `o` ON (`s`.`order_id` = o.`order_id`)"; ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          167┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription` WHERE  
  `store_id` = '" . (int)$store_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
          173┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription` WHERE  
  `subscription_status_id` = '" . (int)$subscription_sta ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          193┆ [1m[24m$query = $this->db->query("SELECT sh.`date_added`, ss.`name` AS status, sh.`comment`, sh.`notify` 
  FROM `" . DB_PREFIX . "subscription_history` sh LEFT  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          199┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription_history`
  WHERE `subscription_id` = '" . (int)$subscription_id ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          205┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription_history`
  WHERE `subscription_status_id` = '" . (int)$subscrip ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/sale/voucher_theme.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           38┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "voucher_theme` vt LEFT JOIN `" .       
  DB_PREFIX . "voucher_theme_description` vtd ON (vt.`voucher ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           80┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "voucher_theme_description` WHERE       
  `voucher_theme_id` = '" . (int)$voucher_theme_id . "'");[0 ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           38┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "voucher_theme` vt LEFT JOIN `" .       
  DB_PREFIX . "voucher_theme_description` vtd ON (vt.`voucher ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           44┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "voucher_theme` vt LEFT JOIN `" . DB_PREFIX .              
  "voucher_theme_description` `vtd` ON (`vt`.`voucher_theme_id` = `v ... [0m                                            
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           80┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "voucher_theme_description` WHERE       
  `voucher_theme_id` = '" . (int)$voucher_theme_id . "'");[0 ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           90┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "voucher_theme`");[0m
                                                                              
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/setting/cron.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           27┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "cron` WHERE `cron_id` = '" .  
  (int)$cron_id . "'");[0m                                                                                              
            ⋮┆----------------------------------------
           33┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "cron` WHERE `code` = '" .     
  $this->db->escape($code) . "' LIMIT 1");[0m                                                                           
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           27┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "cron` WHERE `cron_id` = '" .  
  (int)$cron_id . "'");[0m                                                                                              
            ⋮┆----------------------------------------
           33┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "cron` WHERE `code` = '" .     
  $this->db->escape($code) . "' LIMIT 1");[0m                                                                           
            ⋮┆----------------------------------------
           39┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "cron`";[0m
            ⋮┆----------------------------------------
           80┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "cron`");[0m
                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/setting/event.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           23┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "event` WHERE `event_id` = '" .         
  (int)$event_id . "'");[0m                                                                                             
            ⋮┆----------------------------------------
           29┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "event` WHERE `code` = '" .    
  $this->db->escape($code) . "' LIMIT 1");[0m                                                                           
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           23┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "event` WHERE `event_id` = '" .         
  (int)$event_id . "'");[0m                                                                                             
            ⋮┆----------------------------------------
           29┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "event` WHERE `code` = '" .    
  $this->db->escape($code) . "' LIMIT 1");[0m                                                                           
            ⋮┆----------------------------------------
           35┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "event`";[0m
            ⋮┆----------------------------------------
           76┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "event`");[0m
                                                                                   
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/setting/extension.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension` WHERE `type` = '" .         
  $this->db->escape($type) . "' ORDER BY `code` ASC");[0m                                                               
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension` WHERE `type` = '" .         
  $this->db->escape($type) . "' AND `code` = '" . $this->db->es ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           23┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "extension` WHERE     
  `extension` = '" . $this->db->escape($extension) . "'"); ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           58┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension_install` WHERE               
  `extension_install_id` = '" . (int)$extension_install_id . "'");[0 ... [0m                                            
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           64┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension_install` WHERE               
  `extension_download_id` = '" . (int)$extension_download_id . "'"); ... [0m                                            
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           70┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension_install` WHERE `code` = '" . 
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
          138┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension_path` WHERE                  
  `extension_install_id` = '" . (int)$extension_install_id . "' ORDER BY ... [0m                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          144┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension_path` WHERE `path` LIKE '" . 
  $this->db->escape($path) . "' ORDER BY `path` ASC"); ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          150┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "extension_path` WHERE
  `path` LIKE '" . $this->db->escape($path) . "'");[0 ... [0m                                                           
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT DISTINCT `extension` FROM `" . DB_PREFIX . "extension`");[0m
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension` WHERE `type` = '" .         
  $this->db->escape($type) . "' ORDER BY `code` ASC");[0m                                                               
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension` WHERE `type` = '" .         
  $this->db->escape($type) . "' AND `code` = '" . $this->db->es ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           23┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "extension` WHERE     
  `extension` = '" . $this->db->escape($extension) . "'"); ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           58┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension_install` WHERE               
  `extension_install_id` = '" . (int)$extension_install_id . "'");[0 ... [0m                                            
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           64┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension_install` WHERE               
  `extension_download_id` = '" . (int)$extension_download_id . "'"); ... [0m                                            
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           70┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension_install` WHERE `code` = '" . 
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
           76┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "extension_install`";[0m
            ⋮┆----------------------------------------
          118┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "extension_install`";[0m
            ⋮┆----------------------------------------
          138┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension_path` WHERE                  
  `extension_install_id` = '" . (int)$extension_install_id . "' ORDER BY ... [0m                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          144┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension_path` WHERE `path` LIKE '" . 
  $this->db->escape($path) . "' ORDER BY `path` ASC"); ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          150┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "extension_path` WHERE
  `path` LIKE '" . $this->db->escape($path) . "'");[0 ... [0m                                                           
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/setting/module.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           23┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "module` WHERE `module_id` = '" .       
  (int)$module_id . "'");[0m                                                                                            
            ⋮┆----------------------------------------
           39┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "module` WHERE `code` = '" .            
  $this->db->escape($code) . "' ORDER BY `name`");[0m                                                                   
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           23┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "module` WHERE `module_id` = '" .       
  (int)$module_id . "'");[0m                                                                                            
            ⋮┆----------------------------------------
           33┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "module` ORDER BY `code`");[0m
            ⋮┆----------------------------------------
           39┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "module` WHERE `code` = '" .            
  $this->db->escape($code) . "' ORDER BY `name`");[0m                                                                   
                                                                                 
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/setting/setting.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '" .       
  (int)$store_id . "' OR `store_id` = '0' ORDER BY `store_id` ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           13┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '" .       
  (int)$store_id . "' AND `code` = '" . $this->db->escape($co ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           45┆ [1m[24m$query = $this->db->query("SELECT `value` FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '" . 
  (int)$store_id . "' AND `key` = '" . $this->db->escap ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '" .       
  (int)$store_id . "' OR `store_id` = '0' ORDER BY `store_id` ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           13┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '" .       
  (int)$store_id . "' AND `code` = '" . $this->db->escape($co ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           45┆ [1m[24m$query = $this->db->query("SELECT `value` FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '" . 
  (int)$store_id . "' AND `key` = '" . $this->db->escap ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                 
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/setting/startup.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           23┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "startup` WHERE `startup_id` = '" .     
  (int)$startup_id . "'");[0m                                                                                           
            ⋮┆----------------------------------------
           29┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "startup` WHERE `code` = '" .  
  $this->db->escape($code) . "' LIMIT 1");[0m                                                                           
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           23┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "startup` WHERE `startup_id` = '" .     
  (int)$startup_id . "'");[0m                                                                                           
            ⋮┆----------------------------------------
           29┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "startup` WHERE `code` = '" .  
  $this->db->escape($code) . "' LIMIT 1");[0m                                                                           
            ⋮┆----------------------------------------
           35┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "startup`";[0m
            ⋮┆----------------------------------------
           75┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "startup`");[0m
                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/setting/store.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$this->db->query("INSERT INTO `" . DB_PREFIX . "store` SET `name` = '" .                          
  $this->db->escape((string)$data['config_name']) . "', `url` = '" . $this->db-> ... [0m                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           58┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "store` WHERE `store_id` = '" .
  (int)$store_id . "'");[0m                                                                                             
            ⋮┆----------------------------------------
          195┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_layout_id' AND `value` = '" . (int)$layout_ ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          201┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_language' AND `value` = '" . $this->db->esc ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          207┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_currency' AND `value` = '" . $this->db->esc ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          213┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_country_id' AND `value` = '" . (int)$countr ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          219┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_zone_id' AND `value` = '" . (int)$zone_id . ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          225┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_customer_group_id' AND `value` = '" . (int) ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          231┆ [1m[24m$account_query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting`     
  WHERE `key` = 'config_account_id' AND `value` = '" . (int ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          233┆ [1m[24m$checkout_query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting`    
  WHERE `key` = 'config_checkout_id' AND `value` = '" . (i ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          239┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_order_status_id' AND `value` = '" . (int)$o ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           10┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "layout_route` WHERE `store_id` =       
  '0'");[0m                                                                                                             
            ⋮┆----------------------------------------
           58┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "store` WHERE `store_id` = '" .
  (int)$store_id . "'");[0m                                                                                             
            ⋮┆----------------------------------------
           64┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "store` ORDER BY `url`";[0m
            ⋮┆----------------------------------------
          189┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "store`");[0m
            ⋮┆----------------------------------------
          195┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_layout_id' AND `value` = '" . (int)$layout_ ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          201┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_language' AND `value` = '" . $this->db->esc ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          207┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_currency' AND `value` = '" . $this->db->esc ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          213┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_country_id' AND `value` = '" . (int)$countr ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          219┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_zone_id' AND `value` = '" . (int)$zone_id . ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          225┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_customer_group_id' AND `value` = '" . (int) ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          231┆ [1m[24m$account_query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting`     
  WHERE `key` = 'config_account_id' AND `value` = '" . (int ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          233┆ [1m[24m$checkout_query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting`    
  WHERE `key` = 'config_checkout_id' AND `value` = '" . (i ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          239┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "setting` WHERE `key` 
  = 'config_order_status_id' AND `value` = '" . (int)$o ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                             
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/tool/backup.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           27┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . $table . "` LIMIT " . (int)$start . "," .           
  (int)$limit);[0m                                                                                                      
            ⋮┆----------------------------------------
           37┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . $table . "`");[0m
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           27┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . $table . "` LIMIT " . (int)$start . "," .           
  (int)$limit);[0m                                                                                                      
            ⋮┆----------------------------------------
           37┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . $table . "`");[0m
                                                                                   
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/tool/notification.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           19┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "notification` WHERE           
  `notification_id` = '" . (int)$notification_id . "'");[0m                                                             
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           19┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "notification` WHERE           
  `notification_id` = '" . (int)$notification_id . "'");[0m                                                             
            ⋮┆----------------------------------------
           25┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "notification`";[0m
            ⋮┆----------------------------------------
           51┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "notification`";[0m
                                                                             
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/tool/upload.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "upload` WHERE `upload_id` = '" .       
  (int)$upload_id . "'");[0m                                                                                            
            ⋮┆----------------------------------------
           23┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "upload` WHERE `code` = '" .            
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "upload` WHERE `upload_id` = '" .       
  (int)$upload_id . "'");[0m                                                                                            
            ⋮┆----------------------------------------
           23┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "upload` WHERE `code` = '" .            
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
           29┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "upload`";[0m
            ⋮┆----------------------------------------
           89┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "upload`";[0m
                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/user/api.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           39┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api` WHERE `api_id` = '" . (int)$api_id
  . "'");[0m                                                                                                            
            ⋮┆----------------------------------------
           96┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api_ip` WHERE `api_id` = '" .          
  (int)$api_id . "'");[0m                                                                                               
            ⋮┆----------------------------------------
          106┆ [1m[24m$api_ip_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api_ip` WHERE `ip` = '" .       
  $this->db->escape($ip) . "'");[0m                                                                                     
            ⋮┆----------------------------------------
          109┆ [1m[24m$this->db->query("INSERT INTO `" . DB_PREFIX . "api_ip` SET `api_id` = '" . (int)$api_id . "',    
  `ip` = '" . $this->db->escape($ip) . "'");[0m                                                                         
            ⋮┆----------------------------------------
          112┆ [1m[24m$this->db->query("INSERT INTO `" . DB_PREFIX . "api_session` SET `api_id` = '" . (int)$api_id .   
  "', `session_id` = '" . $this->db->escape($session_id)  ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          118┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api_session` WHERE `api_id` = '" .     
  (int)$api_id . "'");[0m                                                                                               
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           39┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api` WHERE `api_id` = '" . (int)$api_id
  . "'");[0m                                                                                                            
            ⋮┆----------------------------------------
           45┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "api`";[0m
            ⋮┆----------------------------------------
           84┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "api`");[0m
            ⋮┆----------------------------------------
           96┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api_ip` WHERE `api_id` = '" .          
  (int)$api_id . "'");[0m                                                                                               
            ⋮┆----------------------------------------
          106┆ [1m[24m$api_ip_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api_ip` WHERE `ip` = '" .       
  $this->db->escape($ip) . "'");[0m                                                                                     
            ⋮┆----------------------------------------
          118┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api_session` WHERE `api_id` = '" .     
  (int)$api_id . "'");[0m                                                                                               
                                                                           
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/user/user.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           33┆ [1m[24m$query = $this->db->query("SELECT *, (SELECT ug.`name` FROM `" . DB_PREFIX . "user_group` ug WHERE
  ug.`user_group_id` = u.`user_group_id`) AS user_grou ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           39┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "user` WHERE `username` = '" .          
  $this->db->escape($username) . "'");[0m                                                                               
            ⋮┆----------------------------------------
           45┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "user` WHERE LCASE(`email`) =  
  '" . $this->db->escape(oc_strtolower($email)) . "'"); ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           51┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "user` WHERE `code` = '" .              
  $this->db->escape($code) . "' AND `code` != ''");[0m                                                                  
            ⋮┆----------------------------------------
          101┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "user` WHERE          
  `user_group_id` = '" . (int)$user_group_id . "'");[0m                                                                 
            ⋮┆----------------------------------------
          107┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "user` WHERE          
  LCASE(`email`) = '" . $this->db->escape(oc_strtolower($email)) ... [0m                                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          125┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "user_login` WHERE `user_id` = '" .     
  (int)$user_id . "' LIMIT " . (int)$start . "," . (int)$li ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          135┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "user_login` WHERE    
  `user_id` = '" . (int)$user_id . "'");[0m                                                                             
            ⋮┆----------------------------------------
          161┆ [1m[24m$query = $this->db->query("SELECT *, (SELECT SUM(total) FROM `" . DB_PREFIX . "user_authorize`    
  WHERE `user_id` = '" . (int)$user_id . "') AS `attempts` ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          179┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "user_authorize` WHERE `user_id` = '" . 
  (int)$user_id . "' LIMIT " . (int)$start . "," . (int ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          189┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS total FROM `" . DB_PREFIX . "user_authorize` WHERE  
  `user_id` = '" . (int)$user_id . "'");[0m                                                                             
                                                                                 
  [36m[22m[24m  /var/www/html/opencart-latest/admin/model/user/user_group.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           19┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "user_group` WHERE             
  `user_group_id` = '" . (int)$user_group_id . "'");[0m                                                                 
            ⋮┆----------------------------------------
           62┆ [1m[24m$user_group_query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "user_group` WHERE  
  `user_group_id` = '" . (int)$user_group_id . "'");[0m                                                                 
            ⋮┆----------------------------------------
           69┆ [1m[24m$this->db->query("UPDATE `" . DB_PREFIX . "user_group` SET `permission` = '" .                    
  $this->db->escape(json_encode($data)) . "' WHERE `user_group_id` = '" .  ... [0m                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           74┆ [1m[24m$user_group_query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "user_group` WHERE  
  `user_group_id` = '" . (int)$user_group_id . "'");[0m                                                                 
            ⋮┆----------------------------------------
           81┆ [1m[24m$this->db->query("UPDATE `" . DB_PREFIX . "user_group` SET `permission` = '" .                    
  $this->db->escape(json_encode($data)) . "' WHERE `user_group_id` = '" .  ... [0m                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           19┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "user_group` WHERE             
  `user_group_id` = '" . (int)$user_group_id . "'");[0m                                                                 
            ⋮┆----------------------------------------
           30┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "user_group` ORDER BY `name`";[0m
            ⋮┆----------------------------------------
           56┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "user_group`");[0m
            ⋮┆----------------------------------------
           62┆ [1m[24m$user_group_query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "user_group` WHERE  
  `user_group_id` = '" . (int)$user_group_id . "'");[0m                                                                 
            ⋮┆----------------------------------------
           74┆ [1m[24m$user_group_query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "user_group` WHERE  
  `user_group_id` = '" . (int)$user_group_id . "'");[0m                                                                 
                                                                                   
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/controller/mail/order.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
          136┆ [1m[24m$order_status_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_status` WHERE       
  `order_status_id` = '" . (int)$order_status_id . "' AND `la ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          385┆ [1m[24m$order_status_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_status` WHERE       
  `order_status_id` = '" . (int)$order_status_id . "' AND `la ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           53┆ [1m[24m$product_download_query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX .      
  "product_to_download` WHERE `product_id` = '" . (int)$orde ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          136┆ [1m[24m$order_status_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_status` WHERE       
  `order_status_id` = '" . (int)$order_status_id . "' AND `la ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          385┆ [1m[24m$order_status_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_status` WHERE       
  `order_status_id` = '" . (int)$order_status_id . "' AND `la ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          468┆ [1m[24m$order_status_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_status` WHERE       
  `order_status_id` = '" . (int)$order_status_id . "' AND `la ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                     
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/controller/mail/voucher.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           12┆ [1m[24m$voucher_query = $this->db->query("SELECT *, vtd.name AS theme FROM `" . DB_PREFIX . "voucher` v  
  LEFT JOIN `" . DB_PREFIX . "voucher_theme` vt ON (v.`v ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/account/api.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api` WHERE `username` = '" .           
  $this->db->escape($username) . "' AND `key` = '" . $this->db->e ... [0m                                               
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api_ip` WHERE `api_id` = '" .          
  (int)$api_id . "'");[0m                                                                                               
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api` WHERE `username` = '" .           
  $this->db->escape($username) . "' AND `key` = '" . $this->db->e ... [0m                                               
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api_ip` WHERE `api_id` = '" .          
  (int)$api_id . "'");[0m                                                                                               
                                                                                        
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/account/custom_field.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field` cf LEFT JOIN `" .        
  DB_PREFIX . "custom_field_description` cfd ON (cf.`custom_fi ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           16┆ [1m[24m$custom_field_query = $this->db->query("SELECT * FROM `" . DB_PREFIX .                            
  "custom_field_customer_group` cfcg LEFT JOIN `" . DB_PREFIX . "custom_field` cf  ... [0m                              
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field` cf LEFT JOIN `" .        
  DB_PREFIX . "custom_field_description` cfd ON (cf.`custom_fi ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           14┆ [1m[24m$custom_field_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field` cf LEFT JOIN
  `" . DB_PREFIX . "custom_field_description` cfd ON ( ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           16┆ [1m[24m$custom_field_query = $this->db->query("SELECT * FROM `" . DB_PREFIX .                            
  "custom_field_customer_group` cfcg LEFT JOIN `" . DB_PREFIX . "custom_field` cf  ... [0m                              
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           23┆ [1m[24m$custom_field_value_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "custom_field_value` 
  cfv LEFT JOIN `" . DB_PREFIX . "custom_field_value_de ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/account/customer_group.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "customer_group` cg LEFT JOIN  
  `" . DB_PREFIX . "customer_group_description` cgd ON ( ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "customer_group` cg LEFT JOIN  
  `" . DB_PREFIX . "customer_group_description` cgd ON ( ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "customer_group` cg LEFT JOIN `" .      
  DB_PREFIX . "customer_group_description` cgd ON (cg.`custo ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/account/download.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           14┆ [1m[24m$query = $this->db->query("SELECT d.`filename`, d.`mask` FROM `" . DB_PREFIX . "order` o LEFT JOIN
  `" . DB_PREFIX . "order_product` op ON (o.`order_id` ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           40┆ [1m[24m$query = $this->db->query("SELECT DISTINCT d.`download_id`, o.`order_id`, o.`date_added`,         
  dd.`name`, d.`filename` FROM `" . DB_PREFIX . "order` o LEFT  ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/account/gdpr.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           13┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "gdpr` WHERE `gdpr_id` = '" .           
  (int)$gdpr_id . "'");[0m                                                                                              
            ⋮┆----------------------------------------
           19┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "gdpr` WHERE `code` = '" .              
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
           25┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "gdpr` WHERE `email` = '" .             
  $this->db->escape($email) . "'");[0m                                                                                  
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           13┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "gdpr` WHERE `gdpr_id` = '" .           
  (int)$gdpr_id . "'");[0m                                                                                              
            ⋮┆----------------------------------------
           19┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "gdpr` WHERE `code` = '" .              
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
           25┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "gdpr` WHERE `email` = '" .             
  $this->db->escape($email) . "'");[0m                                                                                  
            ⋮┆----------------------------------------
           31┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "gdpr` WHERE `status` = '2' AND         
  DATE(`date_added`) <= DATE('" . $this->db->escape(date('Y-m-d ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                 
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/account/order.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$order_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order` WHERE `order_id` = '" .   
  (int)$order_id . "' AND `customer_id` = '" . (int)$this ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          113┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order` WHERE `customer_id` = '" .      
  (int)$this->customer->getId() . "' AND `order_status_id` > ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          127┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order` WHERE `subscription_id` = '" .  
  (int)$subscription_id . "' AND `customer_id` = '" . (i ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          133┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE         
  `subscription_id` = '" . (int)$subscription_id . "' AND `cust ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          139┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_product` WHERE `order_id` = '" . 
  (int)$order_id . "' AND `order_product_id` = '" . (in ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          145┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_product` WHERE `order_id` = '" . 
  (int)$order_id . "'");[0m                                                                                             
            ⋮┆----------------------------------------
          151┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_option` WHERE `order_id` = '" .  
  (int)$order_id . "' AND `order_product_id` = '" . (int ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          157┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_subscription` WHERE `order_id` = 
  '" . (int)$order_id . "' AND `order_product_id` = '"  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          163┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_voucher` WHERE `order_id` = '" . 
  (int)$order_id . "'");[0m                                                                                             
            ⋮┆----------------------------------------
          169┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_total` WHERE `order_id` = '" .   
  (int)$order_id . "' ORDER BY `sort_order`");[0m                                                                       
            ⋮┆----------------------------------------
          175┆ [1m[24m$query = $this->db->query("SELECT `date_added`, os.`name` AS status, oh.`comment`, oh.`notify`    
  FROM `" . DB_PREFIX . "order_history` oh LEFT JOIN `" .  ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          181┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_history` WHERE 
  `order_id` = '" . (int)$order_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
          201┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_product` op    
  LEFT JOIN `" . DB_PREFIX . "order` o ON (op.`order_id` = ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          211┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_product` WHERE 
  `order_id` = '" . (int)$order_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
          221┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_voucher` WHERE 
  `order_id` = '" . (int)$order_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$order_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order` WHERE `order_id` = '" .   
  (int)$order_id . "' AND `customer_id` = '" . (int)$this ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
            8┆ [1m[24m$country_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "country` WHERE `country_id` =  
  '" . (int)$order_query->row['payment_country_id'] . "' ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           18┆ [1m[24m$zone_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone` WHERE `zone_id` = '" .      
  (int)$order_query->row['payment_zone_id'] . "'");[0m                                                                  
            ⋮┆----------------------------------------
           26┆ [1m[24m$country_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "country` WHERE country_id = '" 
  . (int)$order_query->row['shipping_country_id'] . "'" ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           36┆ [1m[24m$zone_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone` WHERE `zone_id` = '" .      
  (int)$order_query->row['shipping_zone_id'] . "'");[0m                                                                 
            ⋮┆----------------------------------------
          113┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order` WHERE `customer_id` = '" .      
  (int)$this->customer->getId() . "' AND `order_status_id` > ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          127┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order` WHERE `subscription_id` = '" .  
  (int)$subscription_id . "' AND `customer_id` = '" . (i ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          133┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` WHERE         
  `subscription_id` = '" . (int)$subscription_id . "' AND `cust ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          139┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_product` WHERE `order_id` = '" . 
  (int)$order_id . "' AND `order_product_id` = '" . (in ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          145┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_product` WHERE `order_id` = '" . 
  (int)$order_id . "'");[0m                                                                                             
            ⋮┆----------------------------------------
          151┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_option` WHERE `order_id` = '" .  
  (int)$order_id . "' AND `order_product_id` = '" . (int ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          157┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_subscription` WHERE `order_id` = 
  '" . (int)$order_id . "' AND `order_product_id` = '"  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          163┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_voucher` WHERE `order_id` = '" . 
  (int)$order_id . "'");[0m                                                                                             
            ⋮┆----------------------------------------
          169┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_total` WHERE `order_id` = '" .   
  (int)$order_id . "' ORDER BY `sort_order`");[0m                                                                       
            ⋮┆----------------------------------------
          175┆ [1m[24m$query = $this->db->query("SELECT `date_added`, os.`name` AS status, oh.`comment`, oh.`notify`    
  FROM `" . DB_PREFIX . "order_history` oh LEFT JOIN `" .  ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          181┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_history` WHERE 
  `order_id` = '" . (int)$order_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
          191┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order` o WHERE       
  `customer_id` = '" . (int)$this->customer->getId() . "' AND ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          201┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_product` op    
  LEFT JOIN `" . DB_PREFIX . "order` o ON (op.`order_id` = ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          211┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_product` WHERE 
  `order_id` = '" . (int)$order_id . "'");[0m                                                                           
            ⋮┆----------------------------------------
          221┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "order_voucher` WHERE 
  `order_id` = '" . (int)$order_id . "'");[0m                                                                           
                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/account/payment_method.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           21┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "customer_payment` WHERE `customer_id` =
  '" . (int)$customer_id . "' AND `customer_payment_id ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           27┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "customer_payment` WHERE `customer_id` =
  '" . (int)$customer_id . "'");[0m                                                                                     
                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/account/reward.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "customer_reward` WHERE `customer_id` = '" .               
  (int)$this->customer->getId() . "'";[0m                                                                               
            ⋮┆----------------------------------------
           43┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "customer_reward`     
  WHERE `customer_id` = '" . (int)$this->customer->getId()  ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           49┆ [1m[24m$query = $this->db->query("SELECT SUM(`points`) AS `total` FROM `" . DB_PREFIX . "customer_reward`
  WHERE `customer_id` = '" . (int)$this->customer->get ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                        
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/account/subscription.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            7┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription` `s` WHERE                
  `subscription_id` = '" . (int)$subscription_id . "' AND `customer_id ... [0m                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           22┆ [1m[24m$query = $this->db->query("SELECT * FROM  `" . DB_PREFIX . "subscription` WHERE `order_id` = '" . 
  (int)$order_id . "' AND `order_product_id` = '" . (in ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           43┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription` WHERE `customer_id` = '" 
  . (int)$this->customer->getId() . "' AND `subscriptio ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           59┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription` WHERE  
  `customer_id` = '" . (int)$this->customer->getId() . " ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           65┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription` WHERE  
  `customer_id` = '" . (int)$this->customer->getId() . " ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT sh.`date_added`, ss.`name` AS status, sh.`comment`, sh.`notify` 
  FROM `" . DB_PREFIX . "subscription_history` `sh` LEF ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           85┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription_history`
  WHERE `subscription_id` = '" . (int)$subscription_id ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            7┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription` `s` WHERE                
  `subscription_id` = '" . (int)$subscription_id . "' AND `customer_id ... [0m                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           22┆ [1m[24m$query = $this->db->query("SELECT * FROM  `" . DB_PREFIX . "subscription` WHERE `order_id` = '" . 
  (int)$order_id . "' AND `order_product_id` = '" . (in ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           43┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription` WHERE `customer_id` = '" 
  . (int)$this->customer->getId() . "' AND `subscriptio ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           49┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription` WHERE  
  `customer_id` = '" . (int)$this->customer->getId() . " ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           59┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription` WHERE  
  `customer_id` = '" . (int)$this->customer->getId() . " ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           65┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription` WHERE  
  `customer_id` = '" . (int)$this->customer->getId() . " ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           79┆ [1m[24m$query = $this->db->query("SELECT sh.`date_added`, ss.`name` AS status, sh.`comment`, sh.`notify` 
  FROM `" . DB_PREFIX . "subscription_history` `sh` LEF ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           85┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "subscription_history`
  WHERE `subscription_id` = '" . (int)$subscription_id ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                       
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/account/transaction.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "customer_transaction` WHERE `customer_id` = '" .          
  (int)$this->customer->getId() . "'";[0m                                                                               
            ⋮┆----------------------------------------
           43┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "customer_transaction`
  WHERE `customer_id` = '" . (int)$this->customer->get ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           49┆ [1m[24m$query = $this->db->query("SELECT SUM(`amount`) AS `total` FROM `" . DB_PREFIX .                  
  "customer_transaction` WHERE `customer_id` = '" . (int)$this->customer ... [0m                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/account/wishlist.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           15┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "customer_wishlist` WHERE `customer_id` 
  = '" . (int)$this->customer->getId() . "'");[0m                                                                       
            ⋮┆----------------------------------------
           21┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "customer_wishlist`   
  WHERE `customer_id` = '" . (int)$this->customer->getId( ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/catalog/category.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "category` c LEFT JOIN `" .    
  DB_PREFIX . "category_description` cd ON (c.`category_id ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category` c LEFT JOIN `" . DB_PREFIX . 
  "category_description` cd ON (c.`category_id` = cd.`c ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           19┆ [1m[24m$query = $this->db->query("SELECT `filter_id` FROM `" . DB_PREFIX . "category_filter` WHERE       
  `category_id` = '" . (int)$category_id . "'");[0m                                                                     
            ⋮┆----------------------------------------
           56┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_to_layout` WHERE `category_id`
  = '" . (int)$category_id . "' AND `store_id` = '" .  ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "category` c LEFT JOIN `" .    
  DB_PREFIX . "category_description` cd ON (c.`category_id ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category` c LEFT JOIN `" . DB_PREFIX . 
  "category_description` cd ON (c.`category_id` = cd.`c ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           19┆ [1m[24m$query = $this->db->query("SELECT `filter_id` FROM `" . DB_PREFIX . "category_filter` WHERE       
  `category_id` = '" . (int)$category_id . "'");[0m                                                                     
            ⋮┆----------------------------------------
           28┆ [1m[24m$filter_group_query = $this->db->query("SELECT DISTINCT f.`filter_group_id`, fgd.`name`,          
  fg.`sort_order` FROM `" . DB_PREFIX . "filter` f LEFT JOIN `"  ... [0m                                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           33┆ [1m[24m$filter_query = $this->db->query("SELECT DISTINCT f.`filter_id`, fd.`name` FROM `" . DB_PREFIX .  
  "filter` f LEFT JOIN `" . DB_PREFIX . "filter_descript ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           56┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_to_layout` WHERE `category_id`
  = '" . (int)$category_id . "' AND `store_id` = '" .  ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                       
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/catalog/information.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "information` i LEFT JOIN `" . 
  DB_PREFIX . "information_description` id ON (i.`infor ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "information_to_layout` WHERE           
  `information_id` = '" . (int)$information_id . "' AND `store_id ... [0m                                               
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "information` i LEFT JOIN `" . 
  DB_PREFIX . "information_description` id ON (i.`infor ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "information` i LEFT JOIN `" . DB_PREFIX
  . "information_description` id ON (i.`information_id ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "information_to_layout` WHERE           
  `information_id` = '" . (int)$information_id . "' AND `store_id ... [0m                                               
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                        
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/catalog/manufacturer.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "manufacturer` m LEFT JOIN `" .         
  DB_PREFIX . "manufacturer_to_store` m2s ON (m.`manufacturer_i ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           56┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "manufacturer_to_layout` WHERE          
  `manufacturer_id` = '" . (int)$manufacturer_id . "' AND `store ... [0m                                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "manufacturer` m LEFT JOIN `" .         
  DB_PREFIX . "manufacturer_to_store` m2s ON (m.`manufacturer_i ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "manufacturer` m LEFT JOIN `" . DB_PREFIX .                
  "manufacturer_to_store` m2s ON (m.`manufacturer_id` = m2s.`manufactu ... [0m                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           56┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "manufacturer_to_layout` WHERE          
  `manufacturer_id` = '" . (int)$manufacturer_id . "' AND `store ... [0m                                                
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/catalog/review.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           19┆ [1m[24m$query = $this->db->query("SELECT r.`author`, r.`rating`, r.`text`, r.`date_added` FROM `" .      
  DB_PREFIX . "review` r LEFT JOIN `" . DB_PREFIX . "product ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           25┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "review` r LEFT JOIN  
  `" . DB_PREFIX . "product` p ON (r.`product_id` = p.`p ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           19┆ [1m[24m$query = $this->db->query("SELECT r.`author`, r.`rating`, r.`text`, r.`date_added` FROM `" .      
  DB_PREFIX . "review` r LEFT JOIN `" . DB_PREFIX . "product ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           25┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "review` r LEFT JOIN  
  `" . DB_PREFIX . "product` p ON (r.`product_id` = p.`p ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                             
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/catalog/subscription_plan.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription_plan` `sp` LEFT JOIN `" . 
  DB_PREFIX . "subscription_plan_description` `spd` ON  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription_plan` `sp` LEFT JOIN `" . 
  DB_PREFIX . "subscription_plan_description` `spd` ON  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "subscription_plan` `sp` LEFT JOIN `" . DB_PREFIX .        
  "subscription_plan_description` `spd` ON (`sp`.`subscription ... [0m                                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           52┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX .                       
  "subscription_plan`");[0m                                                                                             
                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/checkout/voucher.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           17┆ [1m[24m$voucher_query = $this->db->query("SELECT *, vtd.`name` AS theme FROM `" . DB_PREFIX . "voucher` v
  LEFT JOIN `" . DB_PREFIX . "voucher_theme` vt ON (v. ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/checkout/voucher_theme.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "voucher_theme` vt LEFT JOIN `" .       
  DB_PREFIX . "voucher_theme_description` vtd ON (vt.`voucher ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "voucher_theme` vt LEFT JOIN `" .       
  DB_PREFIX . "voucher_theme_description` vtd ON (vt.`voucher ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "voucher_theme` vt LEFT JOIN `" . DB_PREFIX .              
  "voucher_theme_description` vtd ON (vt.`voucher_theme_id` = vtd.`v ... [0m                                            
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                 
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/design/banner.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "banner` b LEFT JOIN `" . DB_PREFIX .   
  "banner_image` bi ON (b.`banner_id` = bi.`banner_id`) W ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "banner` b LEFT JOIN `" . DB_PREFIX .   
  "banner_image` bi ON (b.`banner_id` = bi.`banner_id`) W ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                 
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/design/layout.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "layout_route` WHERE '" .               
  $this->db->escape($route) . "' LIKE `route` AND `store_id` = '" . ( ... [0m                                           
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           15┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "layout_module` WHERE `layout_id` = '" .
  (int)$layout_id . "' AND `position` = '" . $this->db ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "layout_route` WHERE '" .               
  $this->db->escape($route) . "' LIKE `route` AND `store_id` = '" . ( ... [0m                                           
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           15┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "layout_module` WHERE `layout_id` = '" .
  (int)$layout_id . "' AND `position` = '" . $this->db ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/design/seo_url.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE (`keyword` = '" .       
  $this->db->escape($keyword) . "' OR `keyword` LIKE '" . $th ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE `key` = '" .            
  $this->db->escape($key) . "' AND `value` = '" . $this->db->escap ... [0m                                              
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE (`keyword` = '" .       
  $this->db->escape($keyword) . "' OR `keyword` LIKE '" . $th ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "seo_url` WHERE `key` = '" .            
  $this->db->escape($key) . "' AND `value` = '" . $this->db->escap ... [0m                                              
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/design/theme.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "theme` WHERE `store_id` = '" .         
  (int)$this->config->get('config_store_id') . "' AND `route` = ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "theme` WHERE `store_id` = '" .         
  (int)$this->config->get('config_store_id') . "' AND `route` = ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                      
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/design/translation.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "translation` WHERE `store_id` = '" .   
  (int)$this->config->get('config_store_id') . "' AND `la ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "translation` WHERE `store_id` = '" .   
  (int)$this->config->get('config_store_id') . "' AND `la ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                        
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/localisation/country.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT *, `c`.`name` FROM `" . DB_PREFIX . "country` `c` LEFT JOIN `" .
  DB_PREFIX . "address_format` af ON (`c`.`address_for ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "country` WHERE `iso_code_2` = '" .                        
  $this->db->escape($iso_code_2) . "' AND `status` = '1'";[0m                                                           
            ⋮┆----------------------------------------
           27┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "country` WHERE `iso_code_3` = '" .                        
  $this->db->escape($iso_code_3) . "' AND `status` = '1'";[0m                                                           
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT *, `c`.`name` FROM `" . DB_PREFIX . "country` `c` LEFT JOIN `" .
  DB_PREFIX . "address_format` af ON (`c`.`address_for ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "country` WHERE `iso_code_2` = '" .                        
  $this->db->escape($iso_code_2) . "' AND `status` = '1'";[0m                                                           
            ⋮┆----------------------------------------
           27┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "country` WHERE `iso_code_3` = '" .                        
  $this->db->escape($iso_code_3) . "' AND `status` = '1'";[0m                                                           
            ⋮┆----------------------------------------
           43┆ [1m[24m$sql = "SELECT *, c.`name` FROM `" . DB_PREFIX . "country` c LEFT JOIN `" . DB_PREFIX .           
  "address_format` `af` ON (c.`address_format_id` = af.`address_f ... [0m                                               
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                         
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/localisation/currency.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           11┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "currency` WHERE `currency_id` 
  = '" . $this->db->escape($currency_id) . "'");[0m                                                                     
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "currency` WHERE `code` = '" . 
  $this->db->escape($currency) . "' AND `status` = '1'" ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           11┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "currency` WHERE `currency_id` 
  = '" . $this->db->escape($currency_id) . "'");[0m                                                                     
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "currency` WHERE `code` = '" . 
  $this->db->escape($currency) . "' AND `status` = '1'" ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           23┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "currency` WHERE `status` = '1' ORDER BY `title` ASC";[0m
                                                                                         
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/localisation/language.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "language` WHERE `language_id` = '" .   
  (int)$language_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "language` WHERE `code` = '" .          
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "language` WHERE `language_id` = '" .   
  (int)$language_id . "'");[0m                                                                                          
            ⋮┆----------------------------------------
           37┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "language` WHERE `code` = '" .          
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
           59┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "language` WHERE `status` = '1' ORDER BY `sort_order`,     
  `name`";[0m                                                                                                           
                                                                                         
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/localisation/location.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT `location_id`, `name`, `address`, `geocode`, `telephone`,       
  `image`, `open`, `comment` FROM `" . DB_PREFIX . "location` ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT `location_id`, `name`, `address`, `geocode`, `telephone`,       
  `image`, `open`, `comment` FROM `" . DB_PREFIX . "location` ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                             
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/localisation/order_status.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_status` WHERE `order_status_id` =
  '" . (int)$order_status_id . "' AND `language_id` =  ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_status` WHERE `order_status_id` =
  '" . (int)$order_status_id . "' AND `language_id` =  ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$sql = "SELECT `order_status_id`, `name` FROM `" . DB_PREFIX . "order_status` WHERE `language_id` 
  = '" . (int)$this->config->get('config_language_id')  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                              
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/localisation/return_reason.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "return_reason` WHERE `language_id` = '" .                 
  (int)$this->config->get('config_language_id') . "' ORDER BY `name`"; ... [0m                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                             
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/localisation/stock_status.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "stock_status` WHERE `stock_status_id` =
  '" . (int)$stock_status_id . "' AND `language_id` =  ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "stock_status` WHERE `stock_status_id` =
  '" . (int)$stock_status_id . "' AND `language_id` =  ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "stock_status` WHERE `language_id` = '" .                  
  (int)$this->config->get('config_language_id') . "' ORDER BY `name`";[ ... [0m                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/localisation/subscription_status.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription_status` WHERE             
  `subscription_status_id` = '" . (int)$subscription_status_id . "' ... [0m                                             
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "subscription_status` WHERE             
  `subscription_status_id` = '" . (int)$subscription_status_id . "' ... [0m                                             
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$sql = "SELECT `subscription_status_id`, `name` FROM `" . DB_PREFIX . "subscription_status` WHERE 
  `language_id` = '" . (int)$this->config->get('config_ ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                     
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/localisation/zone.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone` WHERE `zone_id` = '" .           
  (int)$zone_id . "' AND `status` = '1'");[0m                                                                           
            ⋮┆----------------------------------------
           11┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "zone` WHERE `country_id` = '" . (int)$country_id . "' AND 
  `status` = '1' ORDER BY `name`";[0m                                                                                   
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone` WHERE `zone_id` = '" .           
  (int)$zone_id . "' AND `status` = '1'");[0m                                                                           
            ⋮┆----------------------------------------
           11┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "zone` WHERE `country_id` = '" . (int)$country_id . "' AND 
  `status` = '1' ORDER BY `name`";[0m                                                                                   
                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/marketing/coupon.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            7┆ [1m[24m$coupon_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "coupon` WHERE `code` = '" .     
  $this->db->escape($code) . "' AND ((`date_start` = '0000- ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          102┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "coupon_history` ch   
  LEFT JOIN `" . DB_PREFIX . "coupon` c ON (ch.`coupon_id ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          108┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "coupon_history` ch   
  LEFT JOIN `" . DB_PREFIX . "coupon` c ON (ch.`coupon_id ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            7┆ [1m[24m$coupon_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "coupon` WHERE `code` = '" .     
  $this->db->escape($code) . "' AND ((`date_start` = '0000- ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           35┆ [1m[24m$coupon_product_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "coupon_product` WHERE   
  `coupon_id` = '" . (int)$coupon_query->row['coupon_id'] ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           44┆ [1m[24m$coupon_category_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "coupon_category` cc    
  LEFT JOIN `" . DB_PREFIX . "category_path` cp ON (cc.`ca ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           61┆ [1m[24m$coupon_category_query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX .       
  "product_to_category` WHERE `product_id` = '" . (int)$produ ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          102┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "coupon_history` ch   
  LEFT JOIN `" . DB_PREFIX . "coupon` c ON (ch.`coupon_id ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          108┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "coupon_history` ch   
  LEFT JOIN `" . DB_PREFIX . "coupon` c ON (ch.`coupon_id ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                       
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/marketing/marketing.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "marketing` WHERE `code` = '" .
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "marketing` WHERE `code` = '" .
  $this->db->escape($code) . "'");[0m                                                                                   
                                                                                     
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/report/statistics.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           11┆ [1m[24m$query = $this->db->query("SELECT `value` FROM `" . DB_PREFIX . "statistics` WHERE `code` = '" .  
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "statistics`");[0m
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT `value` FROM `" . DB_PREFIX . "statistics` WHERE `code` = '" .  
  $this->db->escape($code) . "'");[0m                                                                                   
                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/setting/api.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api` a LEFT JOIN `" . DB_PREFIX .      
  "api_ip` ai ON (a.`api_id` = ai.`api_id`) WHERE a.`usernam ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "api` a LEFT JOIN `" .         
  DB_PREFIX . "api_session` `as` ON (a.`api_id` = `as`.`api_id` ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api_session` WHERE TIMESTAMPADD(HOUR,  
  1, `date_modified`) < NOW() AND `api_id` = '" . (int)$ ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           23┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api_session` WHERE TIMESTAMPADD(HOUR,  
  1, `date_modified`) < NOW() AND `api_id` = '" . (int)$ ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api` a LEFT JOIN `" . DB_PREFIX .      
  "api_ip` ai ON (a.`api_id` = ai.`api_id`) WHERE a.`usernam ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "api` a LEFT JOIN `" .         
  DB_PREFIX . "api_session` `as` ON (a.`api_id` = `as`.`api_id` ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api_session` WHERE TIMESTAMPADD(HOUR,  
  1, `date_modified`) < NOW() AND `api_id` = '" . (int)$ ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           23┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "api_session` WHERE TIMESTAMPADD(HOUR,  
  1, `date_modified`) < NOW() AND `api_id` = '" . (int)$ ... [0m                                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/setting/cron.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           13┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "cron` WHERE `cron_id` = '" .  
  (int)$cron_id . "'");[0m                                                                                              
            ⋮┆----------------------------------------
           19┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "cron` WHERE `code` = '" .     
  $this->db->escape($code) . "' LIMIT 1");[0m                                                                           
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           13┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "cron` WHERE `cron_id` = '" .  
  (int)$cron_id . "'");[0m                                                                                              
            ⋮┆----------------------------------------
           19┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "cron` WHERE `code` = '" .     
  $this->db->escape($code) . "' LIMIT 1");[0m                                                                           
            ⋮┆----------------------------------------
           25┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "cron` ORDER BY `date_modified`         
  DESC");[0m                                                                                                            
            ⋮┆----------------------------------------
           31┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "cron`");[0m
                                                                                 
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/setting/event.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "event` WHERE `status` = '1' ORDER BY   
  `sort_order` ASC");[0m                                                                                                
                                                                                     
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/setting/extension.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension` WHERE `type` = '" .         
  $this->db->escape($type) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension` WHERE `type` = '" .         
  $this->db->escape($type) . "' AND `code` = '" . $this->db->es ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT DISTINCT `extension` FROM `" . DB_PREFIX . "extension`");[0m
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension` WHERE `type` = '" .         
  $this->db->escape($type) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension` WHERE `type` = '" .         
  $this->db->escape($type) . "' AND `code` = '" . $this->db->es ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/setting/module.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "module` WHERE `module_id` = '" .       
  (int)$module_id . "'");[0m                                                                                            
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "module` WHERE `module_id` = '" .       
  (int)$module_id . "'");[0m                                                                                            
                                                                                   
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/setting/setting.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '" .       
  (int)$store_id . "' OR `store_id` = 0 ORDER BY `store_id` A ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           13┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '" .       
  (int)$store_id . "' AND `code` = '" . $this->db->escape($co ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           27┆ [1m[24m$query = $this->db->query("SELECT `value` FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '" . 
  (int)$store_id . "' AND `key` = '" . $this->db->escap ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '" .       
  (int)$store_id . "' OR `store_id` = 0 ORDER BY `store_id` A ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           13┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '" .       
  (int)$store_id . "' AND `code` = '" . $this->db->escape($co ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           27┆ [1m[24m$query = $this->db->query("SELECT `value` FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '" . 
  (int)$store_id . "' AND `key` = '" . $this->db->escap ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                   
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/setting/startup.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "startup` WHERE `status` = '1' ORDER BY 
  `sort_order` ASC");[0m                                                                                                
                                                                                 
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/setting/store.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            5┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "store` WHERE `store_id` = '" .
  (int)$store_id . "'");[0m                                                                                             
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "store` WHERE REPLACE(`url`, 'www.', '')
  = '" . $this->db->escape($url) . "'");[0m                                                                             
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT DISTINCT * FROM `" . DB_PREFIX . "store` WHERE `store_id` = '" .
  (int)$store_id . "'");[0m                                                                                             
            ⋮┆----------------------------------------
           11┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "store` WHERE REPLACE(`url`, 'www.', '')
  = '" . $this->db->escape($url) . "'");[0m                                                                             
            ⋮┆----------------------------------------
           17┆ [1m[24m$sql = "SELECT * FROM `" . DB_PREFIX . "store` ORDER BY `url`";[0m
                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/catalog/model/tool/upload.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           13┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "upload` WHERE code = '" .              
  $this->db->escape($code) . "'");[0m                                                                                   
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           13┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "upload` WHERE code = '" .              
  $this->db->escape($code) . "'");[0m                                                                                   
                                                                                                      
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/controller/currency/ecb.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           66┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                                                        
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/controller/currency/fixer.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           71┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/dashboard/map.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           14┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total`, SUM(o.`total`) AS `amount`, c.`iso_code_2` 
  FROM `" . DB_PREFIX . "order` o LEFT JOIN `" . DB_PRE ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                             
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/fraud/ip.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           33┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "fraud_ip` ORDER BY `ip` ASC LIMIT " .  
  (int)$start . "," . (int)$limit);[0m                                                                                  
            ⋮┆----------------------------------------
           45┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "fraud_ip` WHERE `ip` 
  = '" . $this->db->escape($ip) . "'");[0m                                                                              
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           33┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "fraud_ip` ORDER BY `ip` ASC LIMIT " .  
  (int)$start . "," . (int)$limit);[0m                                                                                  
            ⋮┆----------------------------------------
           39┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "fraud_ip`");[0m
            ⋮┆----------------------------------------
           45┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "fraud_ip` WHERE `ip` 
  = '" . $this->db->escape($ip) . "'");[0m                                                                              
                                                                                                      
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/module/bestseller.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           33┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "product_bestseller` ORDER BY `total`   
  DESC LIMIT " . (int)$start . "," . (int)$limit);[0m                                                                   
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           33┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "product_bestseller` ORDER BY `total`   
  DESC LIMIT " . (int)$start . "," . (int)$limit);[0m                                                                   
            ⋮┆----------------------------------------
           39┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX .                       
  "product_bestseller`");[0m                                                                                            
                                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/report/activity.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$query = $this->db->query("SELECT `key`, `data`, `date_added` FROM `" . DB_PREFIX .               
  "customer_activity` ORDER BY `date_added` DESC LIMIT 0,5");[0m                                                        
                                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/report/coupon.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$sql = "SELECT ch.`coupon_id`, c.`name`, c.`code`, COUNT(DISTINCT ch.`order_id`) AS orders,       
  SUM(ch.`amount`) AS `total` FROM `" . DB_PREFIX . "coupon_h ... [0m                                                   
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           41┆ [1m[24m$sql = "SELECT COUNT(DISTINCT `coupon_id`) AS `total` FROM `" . DB_PREFIX . "coupon_history`";[0m
                                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/report/customer.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           14┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total`, HOUR(`date_added`) AS `hour` FROM `" .     
  DB_PREFIX . "customer` WHERE DATE(`date_added`) = DATE(NO ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           40┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total`, `date_added` FROM `" . DB_PREFIX .         
  "customer` WHERE DATE(`date_added`) >= DATE('" . $this->db->e ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           64┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total`, `date_added` FROM `" . DB_PREFIX .         
  "customer` WHERE DATE(`date_added`) >= DATE('" . $this->db->e ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           86┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total`, `date_added` FROM `" . DB_PREFIX .         
  "customer` WHERE YEAR(`date_added`) = YEAR(NOW()) GROUP BY MO ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           99┆ [1m[24m$sql = "SELECT c.`customer_id`, CONCAT(c.`firstname`, ' ', c.`lastname`) AS `customer`, c.`email`,
  cgd.`name` AS `customer_group`, c.`status`, o.`order ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          121┆ [1m[24m$sql = "SELECT t.`customer_id`, t.`customer`, t.`email`, t.`customer_group`, t.`status`,          
  COUNT(DISTINCT t.`order_id`) AS `orders`, SUM(t.`products`) AS ... [0m                                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          141┆ [1m[24m$sql = "SELECT COUNT(DISTINCT o.`customer_id`) AS `total` FROM `" . DB_PREFIX . "order` o LEFT    
  JOIN `" . DB_PREFIX . "customer` c ON (o.`customer_id` = ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          167┆ [1m[24m$sql = "SELECT cr.`customer_id`, CONCAT(c.`firstname`, ' ', c.`lastname`) AS `customer`,          
  c.`email`, cgd.`name` AS `customer_group`, c.`status`, SUM(cr. ... [0m                                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          201┆ [1m[24m$sql = "SELECT COUNT(DISTINCT cr.`customer_id`) AS `total` FROM `" . DB_PREFIX . "customer_reward`
  cr LEFT JOIN `" . DB_PREFIX . "customer` c ON (cr.`c ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          227┆ [1m[24m$sql = "SELECT ca.`customer_activity_id`, ca.`customer_id`, ca.`key`, ca.`data`, ca.`ip`,         
  ca.`date_added` FROM `" . DB_PREFIX . "customer_activity` ca  ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          271┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "customer_activity` ca LEFT JOIN `" .    
  DB_PREFIX . "customer` c ON (ca.`customer_id` = c.`custo ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          301┆ [1m[24m$sql = "SELECT cs.`customer_id`, cs.`keyword`, cs.`category_id`, cs.`products`, cs.`ip`,          
  cs.`date_added`, CONCAT(c.`firstname`, ' ', c.`lastname`) AS ` ... [0m                                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          349┆ [1m[24m$sql = "SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "customer_search` cs LEFT JOIN `" .      
  DB_PREFIX . "customer` c ON (cs.`customer_id` = c.`custome ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                                 
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/report/customer_subscription.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$sql = "SELECT `s`.`subscription_id`, `s`.`customer_id`, CONCAT(c.`firstname`, ' ', c.`lastname`) 
  AS customer, c.`email`, cgd.`name` AS customer_group, ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           39┆ [1m[24m$sql = "SELECT COUNT(DISTINCT `s`.`customer_id`) AS `total` FROM `" . DB_PREFIX .                 
  "subscription_transaction` st LEFT JOIN `" . DB_PREFIX . "subscriptio ... [0m                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/report/customer_transaction.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$sql = "SELECT ct.`customer_id`, CONCAT(c.`firstname`, ' ', c.`lastname`) AS customer, c.`email`, 
  cgd.`name` AS customer_group, c.`status`, SUM(ct.`amo ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           39┆ [1m[24m$sql = "SELECT COUNT(DISTINCT ct.`customer_id`) AS `total` FROM `" . DB_PREFIX .                  
  "customer_transaction` ct LEFT JOIN `" . DB_PREFIX . "customer` c ON ( ... [0m                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                     
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/report/marketing.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$sql = "SELECT m.`marketing_id`, m.`name` AS campaign, m.`code`, m.`clicks` AS clicks, (SELECT    
  COUNT(DISTINCT `order_id`) FROM `" . DB_PREFIX . "order` ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           57┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "marketing`");[0m
                                                                                                             
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/report/product_purchased.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$sql = "SELECT op.`name`, op.`model`, SUM(op.`quantity`) AS quantity, SUM((op.`price` + op.`tax`) 
  * op.`quantity`) AS `total` FROM `" . DB_PREFIX . "or ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           41┆ [1m[24m$sql = "SELECT COUNT(DISTINCT op.`product_id`) AS `total` FROM `" . DB_PREFIX . "order_product` op
  LEFT JOIN `" . DB_PREFIX . "order` o ON (op.`order_i ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/report/product_viewed.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           29┆ [1m[24m$query = $this->db->query("SELECT `product_id`, `viewed` FROM `" . DB_PREFIX . "product_viewed`   
  ORDER BY `viewed` DESC LIMIT " . (int)$start . "," . (i ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           29┆ [1m[24m$query = $this->db->query("SELECT `product_id`, `viewed` FROM `" . DB_PREFIX . "product_viewed`   
  ORDER BY `viewed` DESC LIMIT " . (int)$start . "," . (i ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           35┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "product_viewed`");[0m
            ⋮┆----------------------------------------
           41┆ [1m[24m$query = $this->db->query("SELECT SUM(`viewed`) AS `total` FROM `" . DB_PREFIX .                  
  "product_viewed`");[0m                                                                                                
                                                                                                   
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/report/returns.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$sql = "SELECT MIN(r.`date_added`) AS date_start, MAX(r.`date_added`) AS date_end,                
  COUNT(r.`return_id`) AS returns FROM `" . DB_PREFIX . "return` r";[ ... [0m                                           
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           69┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(`date_added`), MONTH(`date_added`), DAY(`date_added`)) AS      
  `total` FROM `" . DB_PREFIX . "return`";[0m                                                                           
            ⋮┆----------------------------------------
           73┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(`date_added`), WEEK(`date_added`)) AS `total` FROM `" .        
  DB_PREFIX . "return`";[0m                                                                                             
            ⋮┆----------------------------------------
           76┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(`date_added`), MONTH(`date_added`)) AS `total` FROM `" .       
  DB_PREFIX . "return`";[0m                                                                                             
            ⋮┆----------------------------------------
           79┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(`date_added`)) AS `total` FROM `" . DB_PREFIX . "return`";[0m
                                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/admin/model/report/sale.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            5┆ [1m[24m$sql = "SELECT SUM(`total`) AS `total` FROM `" . DB_PREFIX . "order` WHERE `order_status_id` >    
  '0'";[0m                                                                                                              
            ⋮┆----------------------------------------
           17┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS total, SUM(o.`total`) AS amount, c.`iso_code_2` FROM
  `" . DB_PREFIX . "order` o LEFT JOIN `" . DB_PREFIX  ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           38┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS total, HOUR(`date_added`) AS hour FROM `" .         
  DB_PREFIX . "order` WHERE `order_status_id` IN(" . implode(", ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           70┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS total, `date_added` FROM `" . DB_PREFIX . "order`   
  WHERE `order_status_id` IN(" . implode(",", $implode) . ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          100┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS total, `date_added` FROM `" . DB_PREFIX . "order`   
  WHERE `order_status_id` IN(" . implode(",", $implode) . ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          128┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS total, `date_added` FROM `" . DB_PREFIX . "order`   
  WHERE `order_status_id` IN(" . implode(",", $implode) . ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          141┆ [1m[24m$sql = "SELECT MIN(o.`date_added`) AS date_start, MAX(o.`date_added`) AS date_end, COUNT(*) AS    
  orders, SUM((SELECT SUM(op.`quantity`) FROM `" . DB_PREF ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          207┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(`date_added`), MONTH(`date_added`), DAY(`date_added`)) AS      
  `total` FROM `" . DB_PREFIX . "order`";[0m                                                                            
            ⋮┆----------------------------------------
          211┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(`date_added`), WEEK(`date_added`)) AS `total` FROM `" .        
  DB_PREFIX . "order`";[0m                                                                                              
            ⋮┆----------------------------------------
          214┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(`date_added`), MONTH(`date_added`)) AS `total` FROM `" .       
  DB_PREFIX . "order`";[0m                                                                                              
            ⋮┆----------------------------------------
          217┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(`date_added`)) AS `total` FROM `" . DB_PREFIX . "order`";[0m
            ⋮┆----------------------------------------
          241┆ [1m[24m$sql = "SELECT MIN(o.`date_added`) AS date_start, MAX(o.`date_added`) AS date_end, ot.`title`,    
  SUM(ot.`value`) AS total, COUNT(o.`order_id`) AS `orders ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          305┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(o.`date_added`), MONTH(o.`date_added`), DAY(o.`date_added`),   
  ot.`title`) AS `total` FROM `" . DB_PREFIX . "order` o" ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          309┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(o.`date_added`), WEEK(o.`date_added`), ot.`title`) AS `total`  
  FROM `" . DB_PREFIX . "order` o";[0m                                                                                  
            ⋮┆----------------------------------------
          312┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(o.`date_added`), MONTH(o.`date_added`), ot.`title`) AS `total` 
  FROM `" . DB_PREFIX . "order` o";[0m                                                                                  
            ⋮┆----------------------------------------
          315┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(o.`date_added`), ot.`title`) AS `total` FROM `" . DB_PREFIX .  
  "order` o";[0m                                                                                                        
            ⋮┆----------------------------------------
          341┆ [1m[24m$sql = "SELECT MIN(o.`date_added`) AS date_start, MAX(o.`date_added`) AS date_end, ot.`title`,    
  SUM(ot.`value`) AS total, COUNT(o.`order_id`) AS orders  ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          405┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(o.`date_added`), MONTH(o.`date_added`), DAY(o.`date_added`),   
  ot.`title`) AS `total` FROM `" . DB_PREFIX . "order` o" ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          409┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(o.`date_added`), WEEK(o.`date_added`), ot.`title`) AS `total`  
  FROM `" . DB_PREFIX . "order` o";[0m                                                                                  
            ⋮┆----------------------------------------
          412┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(o.`date_added`), MONTH(o.`date_added`), ot.`title`) AS `total` 
  FROM `" . DB_PREFIX . "order` o";[0m                                                                                  
            ⋮┆----------------------------------------
          415┆ [1m[24m$sql = "SELECT COUNT(DISTINCT YEAR(o.`date_added`), ot.`title`) AS `total` FROM `" . DB_PREFIX .  
  "order` o";[0m                                                                                                        
                                                                                                        
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/controller/currency/ecb.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           11┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/controller/currency/fixer.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           11┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/model/fraud/ip.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           22┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "fraud_ip` WHERE `ip` = '" .            
  $this->db->escape($order_info['ip']) . "'");[0m                                                                       
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           13┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "fraud_ip` WHERE `ip` = '" .            
  $this->db->escape($result['ip']) . "'");[0m                                                                           
            ⋮┆----------------------------------------
           22┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "fraud_ip` WHERE `ip` = '" .            
  $this->db->escape($order_info['ip']) . "'");[0m                                                                       
                                                                                                        
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/model/module/bestseller.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            6┆ [1m[24m$sql = "SELECT *, `pd`.`name`, `p`.`image`, `pb`.`total`, " . $this->statement['discount'] . ", " 
  . $this->statement['special'] . ", " . $this->stateme ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                            
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/model/payment/bank_transfer.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           14┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('payment_bank_transfer_ ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           14┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('payment_bank_transfer_ ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                     
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/model/payment/cheque.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           14┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('payment_cheque_geo_zon ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           14┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('payment_cheque_geo_zon ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/model/payment/cod.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           16┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('payment_cod_geo_zone_i ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           16┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('payment_cod_geo_zone_i ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/model/shipping/flat.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            7┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('shipping_flat_geo_zone ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            7┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('shipping_flat_geo_zone ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/model/shipping/free.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            7┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('shipping_free_geo_zone ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            7┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('shipping_free_geo_zone ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/model/shipping/item.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            7┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('shipping_item_geo_zone ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            7┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('shipping_item_geo_zone ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                      
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/model/shipping/pickup.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
            7┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('shipping_pickup_geo_zo ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            7┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$this->config->get('shipping_pickup_geo_zo ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                      
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/model/shipping/weight.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           15┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$result['geo_zone_id'] . "' AND `country_i ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
            9┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "geo_zone` ORDER BY `name`");[0m
            ⋮┆----------------------------------------
           15┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "zone_to_geo_zone` WHERE `geo_zone_id` =
  '" . (int)$result['geo_zone_id'] . "' AND `country_i ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                   
  [36m[22m[24m  /var/www/html/opencart-latest/extension/opencart/catalog/model/total/coupon.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
          133┆ [1m[24m$this->db->query("INSERT INTO `" . DB_PREFIX . "coupon_history` SET `coupon_id` = '" .            
  (int)$coupon_query->row['coupon_id'] . "', `order_id` = '" . (in ... [0m                                              
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
          110┆ [1m[24m$coupon_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "coupon` WHERE `code` = '" .     
  $this->db->escape($code) . "' AND `status` = '1'");[0m                                                                
                                                                       
  [36m[22m[24m  /var/www/html/opencart-latest/install/cli_cloud.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
          179┆ [1m[24m$table_query = $db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" .     
  $db_database . "' AND TABLE_NAME = '" . $db_prefix . $tab ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                         
  [36m[22m[24m  /var/www/html/opencart-latest/install/cli_install.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
          271┆ [1m[24m$table_query = $db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" .     
  $db_database . "' AND TABLE_NAME = '" . $db_prefix . $tab ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/install/controller/install/promotion.php [0m
       [1m[24mphp.lang.security.curl-ssl-verifypeer-off.curl-ssl-verifypeer-off[0m            
          SSL verification is disabled but should not be (currently CURLOPT_SSL_VERIFYPEER= 0)
          Details: https://sg.run/PJqv                                                        
                                                                                              
           10┆ [1m[24mcurl_setopt($curl, CURLOPT_SSL_VERIFYPEER, 0)[0m;
                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/install/controller/upgrade/upgrade_3.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           28┆ [1m[24m$table_query = $this->db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" 
  . DB_DATABASE . "' AND TABLE_NAME = '" . DB_PREFIX .  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           67┆ [1m[24m$field_query = $this->db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" 
  . DB_DATABASE . "' AND TABLE_NAME = '" . DB_PREFIX .  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          102┆ [1m[24m$field_query = $this->db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" 
  . DB_DATABASE . "' AND TABLE_NAME = '" . DB_PREFIX .  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/install/controller/upgrade/upgrade_4.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           12┆ [1m[24m$query = $this->db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" .     
  DB_DATABASE . "' AND TABLE_NAME = '" . DB_PREFIX . "setti ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           22┆ [1m[24m$query = $this->db->query("SELECT `setting_id`, `value` FROM `" . DB_PREFIX . "setting` WHERE     
  `serialized` = '1' AND `value` LIKE 'a:%'");[0m                                                                       
            ⋮┆----------------------------------------
           33┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "setting` WHERE `store_id` = '0'");[0m
            ⋮┆----------------------------------------
          295┆ [1m[24m$query = $this->db->query("SELECT setting_id FROM `" . DB_PREFIX . "setting` WHERE `store_id` =   
  '0' AND `key` = '" . $this->db->escape($setting['key']) ... [0m                                                       
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          309┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension`");[0m
            ⋮┆----------------------------------------
          313┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "setting` WHERE `code` = '" .           
  $extension['code'] . "'");[0m                                                                                         
            ⋮┆----------------------------------------
          386┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "extension`");[0m
                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/install/controller/upgrade/upgrade_5.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
          231┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "event` WHERE `code` = '" .             
  $this->db->escape($event['code']) . "'");[0m                                                                          
            ⋮┆----------------------------------------
          239┆ [1m[24m$query = $this->db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" .     
  DB_DATABASE . "' AND TABLE_NAME = '" . DB_PREFIX . "event ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/install/controller/upgrade/upgrade_6.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           12┆ [1m[24m$query = $this->db->query("SELECT `customer_id`, `custom_field` FROM `" . DB_PREFIX . "customer`  
  WHERE `custom_field` LIKE 'a:%'");[0m                                                                                 
            ⋮┆----------------------------------------
           21┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "customer_activity` WHERE `data` LIKE   
  'a:%'");[0m                                                                                                           
            ⋮┆----------------------------------------
           30┆ [1m[24m$query = $this->db->query("SELECT `address_id`, `custom_field` FROM `" . DB_PREFIX . "address`    
  WHERE `custom_field` LIKE 'a:%'");[0m                                                                                 
            ⋮┆----------------------------------------
           39┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "module`");[0m
            ⋮┆----------------------------------------
           48┆ [1m[24m$query = $this->db->query("SELECT `order_id`, `custom_field`, `payment_custom_field`,             
  `shipping_custom_field` FROM `" . DB_PREFIX . "order` WHERE `cust ... [0m                                             
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           65┆ [1m[24m$query = $this->db->query("SELECT `user_group_id`, `permission` FROM `" . DB_PREFIX .             
  "user_group`");[0m                                                                                                    
                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/install/controller/upgrade/upgrade_7.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
          158┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category` WHERE `parent_id` = '" .     
  (int)$parent_id . "'");[0m                                                                                            
            ⋮┆----------------------------------------
          167┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '"
  . (int)$parent_id . "' ORDER BY `level` ASC");[0m                                                                     
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           19┆ [1m[24m$query = $this->db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" .     
  DB_DATABASE . "' AND TABLE_NAME = '" . DB_PREFIX . "produ ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           26┆ [1m[24m$query = $this->db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" .     
  DB_DATABASE . "' AND TABLE_NAME = '" . DB_PREFIX . "produ ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           29┆ [1m[24m$language_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "language`");[0m
            ⋮┆----------------------------------------
           33┆ [1m[24m$product_query = $this->db->query("SELECT p.`product_id`, GROUP_CONCAT(DISTINCT pt.`tag` order by 
  pt.`tag` ASC SEPARATOR ',') as `tags` FROM `" . DB_PR ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           45┆ [1m[24m$query = $this->db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" .     
  DB_DATABASE . "' AND TABLE_NAME = '" . DB_PREFIX . "banne ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           48┆ [1m[24m$banner_image_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "banner_image`");[0m
            ⋮┆----------------------------------------
           53┆ [1m[24m$banner_image_description_query = $this->db->query("SELECT * FROM `" . DB_PREFIX .                
  "banner_image_description` WHERE `banner_image_id` = '" . (int)$bann ... [0m                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          109┆ [1m[24m$query = $this->db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" .     
  DB_DATABASE . "' AND TABLE_NAME = '" . DB_PREFIX . $resul ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          123┆ [1m[24m$query = $this->db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" .     
  DB_DATABASE . "' AND TABLE_NAME = '" . DB_PREFIX . $table ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          158┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category` WHERE `parent_id` = '" .     
  (int)$parent_id . "'");[0m                                                                                            
            ⋮┆----------------------------------------
          167┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "category_path` WHERE `category_id` = '"
  . (int)$parent_id . "' ORDER BY `level` ASC");[0m                                                                     
                                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/install/controller/upgrade/upgrade_9.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" .     
  DB_DATABASE . "' AND TABLE_NAME = '" . DB_PREFIX . "order ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           20┆ [1m[24m$query = $this->db->query("SELECT `order_id`, `payment_code`, `payment_method`, `shipping_method`,
  `shipping_code` FROM `" . DB_PREFIX . "order`");[0m                                                                   
            ⋮┆----------------------------------------
           33┆ [1m[24m$order_total_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "order_total` WHERE         
  `order_id` = '" . (int)$result['order_id'] . "' AND `code` =  ... [0m                                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           63┆ [1m[24m$query = $this->db->query("SELECT * FROM information_schema.COLUMNS WHERE TABLE_SCHEMA = '" .     
  DB_DATABASE . "' AND TABLE_NAME = '" . DB_PREFIX . $resul ... [0m                                                     
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/system/library/cache/file.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.frameworks.yii.sql-injection-yii-framework-apps3c[0m
          Detected a formatted string in a Yii SQL operation with a concatenated  value that came from       
          a function argument. This could lead to SQL injection if variables in the SQL statement are        
          not properly sanitized.                                                                            
                                                                                                             
           41┆ [1m[24m$this->delete($key)[0m;
                                                                              
  [36m[22m[24m  /var/www/html/opencart-latest/system/library/cache/mem.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.frameworks.yii.sql-injection-yii-framework-apps3c[0m
          Detected a formatted string in a Yii SQL operation with a concatenated  value that came from       
          a function argument. This could lead to SQL injection if variables in the SQL statement are        
          not properly sanitized.                                                                            
                                                                                                             
           53┆ [1m[24m$this->memcache->delete(CACHE_PREFIX . $key)[0m;
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.frameworks.yii.sql-injection-yii-framework-potential-
       apps3c[0m                                                                                              
          Detected a SQL operation with Yii framework with a concatenated  value. This could lead to          
          SQL injection if variables in the SQL  statement are not properly sanitized.                        
                                                                                                              
           53┆ [1m[24m$this->memcache->delete(CACHE_PREFIX . $key)[0m;
                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/system/library/cache/memcached.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.frameworks.yii.sql-injection-yii-framework-apps3c[0m
          Detected a formatted string in a Yii SQL operation with a concatenated  value that came from       
          a function argument. This could lead to SQL injection if variables in the SQL statement are        
          not properly sanitized.                                                                            
                                                                                                             
           53┆ [1m[24m$this->memcached->delete(CACHE_PREFIX . $key)[0m;
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.frameworks.yii.sql-injection-yii-framework-potential-
       apps3c[0m                                                                                              
          Detected a SQL operation with Yii framework with a concatenated  value. This could lead to          
          SQL injection if variables in the SQL  statement are not properly sanitized.                        
                                                                                                              
           53┆ [1m[24m$this->memcached->delete(CACHE_PREFIX . $key)[0m;
                                                                          
  [36m[22m[24m  /var/www/html/opencart-latest/system/library/cache.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.frameworks.yii.sql-injection-yii-framework-apps3c[0m
          Detected a formatted string in a Yii SQL operation with a concatenated  value that came from       
          a function argument. This could lead to SQL injection if variables in the SQL statement are        
          not properly sanitized.                                                                            
                                                                                                             
           63┆ [1m[24m$this->adaptor->delete($key)[0m;
                                                                              
  [36m[22m[24m  /var/www/html/opencart-latest/system/library/cart/cart.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
          346┆ [1m[24m$query = $this->db->query("SELECT COUNT(*) AS `total` FROM `" . DB_PREFIX . "cart` WHERE `api_id` 
  = '" . (isset($this->session->data['api_id']) ? (int) ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          349┆ [1m[24m$this->db->query("INSERT INTO `" . DB_PREFIX . "cart` SET `api_id` = '" .                         
  (isset($this->session->data['api_id']) ? (int)$this->session->data['api_id']  ... [0m                                 
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          351┆ [1m[24m$this->db->query("UPDATE `" . DB_PREFIX . "cart` SET `quantity` = (`quantity` + " . (int)$quantity
  . ") WHERE `api_id` = '" . (isset($this->session->da ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/system/library/cart/currency.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           17┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "currency`");[0m
                                                                                  
  [36m[22m[24m  /var/www/html/opencart-latest/system/library/cart/customer.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           56┆ [1m[24m$customer_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "customer` WHERE LCASE(`email`)
  = '" . $this->db->escape(oc_strtolower($email)) . "' ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           71┆ [1m[24m$this->db->query("UPDATE `" . DB_PREFIX . "customer` SET `password` = '" .                        
  $this->db->escape(password_hash($password, PASSWORD_DEFAULT)) . "' WHERE `cu ... [0m                                  
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           28┆ [1m[24m$customer_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "customer` WHERE `customer_id` 
  = '" . (int)$this->session->data['customer_id'] . "'  ... [0m                                                         
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           56┆ [1m[24m$customer_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "customer` WHERE LCASE(`email`)
  = '" . $this->db->escape(oc_strtolower($email)) . "' ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          188┆ [1m[24m$query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "address` WHERE `customer_id` = '" .    
  (int)$this->customer_id . "' AND `default` = '1'");[0m                                                                
            ⋮┆----------------------------------------
          203┆ [1m[24m$query = $this->db->query("SELECT SUM(`amount`) AS `total` FROM `" . DB_PREFIX .                  
  "customer_transaction` WHERE `customer_id` = '" . (int)$this->customer ... [0m                                        
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          214┆ [1m[24m$query = $this->db->query("SELECT SUM(`points`) AS `total` FROM `" . DB_PREFIX . "customer_reward`
  WHERE `customer_id` = '" . (int)$this->customer_id . ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/system/library/cart/length.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           17┆ [1m[24m$length_class_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "length_class` mc LEFT JOIN
  `" . DB_PREFIX . "length_class_description` mcd ON ( ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                             
  [36m[22m[24m  /var/www/html/opencart-latest/system/library/cart/tax.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           27┆ [1m[24m$tax_query = $this->db->query("SELECT tr1.`tax_class_id`, tr2.`tax_rate_id`, tr2.`name`,          
  tr2.`rate`, tr2.`type`, tr1.`priority` FROM `" . DB_PREFIX . " ... [0m                                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           49┆ [1m[24m$tax_query = $this->db->query("SELECT tr1.`tax_class_id`, tr2.`tax_rate_id`, tr2.`name`,          
  tr2.`rate`, tr2.`type`, tr1.`priority` FROM `" . DB_PREFIX . " ... [0m                                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           71┆ [1m[24m$tax_query = $this->db->query("SELECT tr1.`tax_class_id`, tr2.`tax_rate_id`, tr2.`name`,          
  tr2.`rate`, tr2.`type`, tr1.`priority` FROM `" . DB_PREFIX . " ... [0m                                                
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
          141┆ [1m[24m$tax_query = $this->db->query("SELECT `name` FROM `" . DB_PREFIX . "tax_rate` WHERE `tax_rate_id` 
  = '" . (int)$tax_rate_id . "'");[0m                                                                                   
                                                                              
  [36m[22m[24m  /var/www/html/opencart-latest/system/library/cart/user.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           58┆ [1m[24m$user_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "user` WHERE `username` = '" .     
  $this->db->escape($username) . "' AND `status` = '1'");[ ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           72┆ [1m[24m$this->db->query("UPDATE `" . DB_PREFIX . "user` SET `password` = '" .                            
  $this->db->escape(password_hash($password, PASSWORD_DEFAULT)) . "' WHERE `user_i ... [0m                              
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           24┆ [1m[24m$user_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "user` WHERE `user_id` = '" .      
  (int)$this->session->data['user_id'] . "' AND `status` = ' ... [0m                                                    
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           34┆ [1m[24m$user_group_query = $this->db->query("SELECT `permission` FROM `" . DB_PREFIX . "user_group` WHERE
  `user_group_id` = '" . (int)$user_query->row['user_g ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           58┆ [1m[24m$user_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "user` WHERE `username` = '" .     
  $this->db->escape($username) . "' AND `status` = '1'");[ ... [0m                                                      
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
           82┆ [1m[24m$user_group_query = $this->db->query("SELECT `permission` FROM `" . DB_PREFIX . "user_group` WHERE
  `user_group_id` = '" . (int)$user_query->row['user_g ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                
  [36m[22m[24m  /var/www/html/opencart-latest/system/library/cart/weight.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           17┆ [1m[24m$weight_class_query = $this->db->query("SELECT * FROM `" . DB_PREFIX . "weight_class` wc LEFT JOIN
  `" . DB_PREFIX . "weight_class_description` wcd ON ( ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/system/library/session/db.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           33┆ [1m[24m$query = $this->db->query("SELECT `data` FROM `" . DB_PREFIX . "session` WHERE `session_id` = '" .
  $this->db->escape($session_id) . "' AND `expire` > ' ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           33┆ [1m[24m$query = $this->db->query("SELECT `data` FROM `" . DB_PREFIX . "session` WHERE `session_id` = '" .
  $this->db->escape($session_id) . "' AND `expire` > ' ... [0m                                                          
            [shortened a long line from output, adjust with --max-chars-per-line]
                                                                                                                    
  [36m[22m[24m  /var/www/html/opencart-latest/system/storage/vendor/aws/aws-sdk-php/src/DoctrineCacheAdapter.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.frameworks.yii.sql-injection-yii-framework-apps3c[0m
          Detected a formatted string in a Yii SQL operation with a concatenated  value that came from       
          a function argument. This could lead to SQL injection if variables in the SQL statement are        
          not properly sanitized.                                                                            
                                                                                                             
           38┆ return [1m[24m$this->cache->delete($key)[0m;
                                                                                                                 
  [36m[22m[24m  /var/www/html/opencart-latest/system/storage/vendor/aws/aws-sdk-php/src/Psr16CacheAdapter.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.frameworks.yii.sql-injection-yii-framework-apps3c[0m
          Detected a formatted string in a Yii SQL operation with a concatenated  value that came from       
          a function argument. This could lead to SQL injection if variables in the SQL statement are        
          not properly sanitized.                                                                            
                                                                                                             
           28┆ [1m[24m$this->cache->delete($key)[0m;
                                                                                                             
  [36m[22m[24m  /var/www/html/opencart-latest/system/storage/vendor/guzzlehttp/promises/src/Coroutine.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
          129┆ [1m[24m$this->currentPromise = Create::promiseFor($yielded)[0m
          130┆ [1m[24m    ->then([$this, '_handleSuccess'], [$this, '_handleFailure']);[0m
            ⋮┆----------------------------------------
          160┆ [1m[24m$nextYield = $this->generator->throw(Create::exceptionFor($reason));[0m
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
          129┆ [1m[24m$this->currentPromise = Create::promiseFor($yielded)[0m
          130┆ [1m[24m    ->then([$this, '_handleSuccess'], [$this, '_handleFailure']);[0m
                                                                                                               
  [36m[22m[24m  /var/www/html/opencart-latest/system/storage/vendor/guzzlehttp/promises/src/EachPromise.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-apps3c[0m 
          Detected a formatted string starting with a SQL operation with a concatenated  value that
          came from a function argument. This could lead to SQL injection if variables in the SQL  
          statement are not properly sanitized.                                                    
                                                                                                   
           56┆ [1m[24m$this->iterable = Create::iterFor($iterable);[0m
            ⋮┆----------------------------------------
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           56┆ [1m[24m$this->iterable = Create::iterFor($iterable);[0m
            ⋮┆----------------------------------------
          159┆ [1m[24m$promise = Create::promiseFor($this->iterable->current());[0m
                                                                                                           
  [36m[22m[24m  /var/www/html/opencart-latest/system/storage/vendor/guzzlehttp/promises/src/Promise.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.lang.security.sql-injection-php-potential-apps3c[0m
          Detected a string starting with a SQL operation with a concatenated  value. This could lead       
          to SQL injection if variables in the SQL  statement are not properly sanitized.                   
                                                                                                            
           45┆ [1m[24m$promise = Create::promiseFor($this->result);[0m
            ⋮┆----------------------------------------
           51┆ [1m[24m$rejection = Create::rejectionFor($this->result);[0m
                                                                                                        
  [36m[22m[24m  /var/www/html/opencart-latest/system/storage/vendor/scssphp/scssphp/src/Compiler.php [0m
       [1m[24mopt.semgrep-custom-rules.semgrep-rules.php.frameworks.yii.sql-injection-yii-framework-apps3c[0m
          Detected a formatted string in a Yii SQL operation with a concatenated  value that came from       
          a function argument. This could lead to SQL injection if variables in the SQL statement are        
          not properly sanitized.                                                                            
                                                                                                             
         5879┆ $path = [1m[24mPath::join($baseDir, $url)[0m;
