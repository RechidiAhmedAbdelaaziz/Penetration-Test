# Misconfigured Regex

- `preg_match\(['"]?.*['"]?\)|preg_replace\(['"]?.*['"]?\)`

```php
221 results - 91 files

admin/controller/catalog/category.php:
  410  
  411: 					if (preg_match('/[^a-zA-Z0-9\/_-]|[\p{Cyrillic}]+/u', $keyword)) {
  412  						$json['error']['keyword_' . $store_id . '_' . $language_id] = $this->language->get('error_keyword_character');

admin/controller/catalog/download.php:
  283  
  284: 		if (preg_match('/[^a-zA-Z0-9\/._-]|[\p{Cyrillic}]+/u', $this->request->post['filename'])) {
  285  			$json['error']['filename'] = $this->language->get('error_filename_character');

  291  
  292: 		if (preg_match('/[^a-zA-Z0-9\/._-]|[\p{Cyrillic}]+/u', $this->request->post['mask'])) {
  293  			$json['error']['mask'] = $this->language->get('error_mask_character');

  456  
  457: 			$extension_allowed = preg_replace('~\r?\n~', "\n", $this->config->get('config_file_ext_allowed'));
  458  

  471  
  472: 			$mime_allowed = preg_replace('~\r?\n~', "\n", $this->config->get('config_file_mime_allowed'));
  473  

admin/controller/catalog/information.php:
  326  
  327: 					if (preg_match('/[^a-zA-Z0-9\/_-]|[\p{Cyrillic}]+/u', $keyword)) {
  328  						$json['error']['keyword_' . $store_id . '_' . $language_id] = $this->language->get('error_keyword_character');

admin/controller/catalog/manufacturer.php:
  320  
  321: 					if (preg_match('/[^a-zA-Z0-9\/_-]|[\p{Cyrillic}]+/u', $keyword)) {
  322  						$json['error']['keyword_' . $store_id . '_' . $language_id] = $this->language->get('error_keyword_character');

admin/controller/catalog/product.php:
  1098  
  1099: 					if (preg_match('/[^a-zA-Z0-9\/_-]|[\p{Cyrillic}]+/u', $keyword)) {
  1100  						$json['error']['keyword_' . $store_id . '_' . $language_id] = $this->language->get('error_keyword_character');

admin/controller/cms/article.php:
  366  
  367: 					if (preg_match('/[^a-zA-Z0-9\/_-]|[\p{Cyrillic}]+/u', $keyword)) {
  368  						$json['error']['keyword_' . $store_id . '_' . $language_id] = $this->language->get('error_keyword_character');

admin/controller/cms/topic.php:
  324  
  325: 					if (preg_match('/[^a-zA-Z0-9\/_-]|[\p{Cyrillic}]+/u', $keyword)) {
  326  						$json['error']['keyword_' . $store_id . '_' . $language_id] = $this->language->get('error_keyword_character');

admin/controller/common/filemanager.php:
  285  					// Sanitize the filename
  286: 					$filename = preg_replace('[/\\?%*:|"<>]', '', basename(html_entity_decode($file['name'], ENT_QUOTES, 'UTF-8')));
  287  

  376  			// Sanitize the folder name
  377: 			$folder = preg_replace('[/\\?%*&:|"<>]', '', basename(html_entity_decode($this->request->post['folder'], ENT_QUOTES, 'UTF-8')));
  378  

admin/controller/common/security.php:
  134  		if (isset($this->request->get['name'])) {
  135: 			$name = preg_replace('[^a-zA-z0-9_]', '', basename(html_entity_decode(trim($this->request->get['name']), ENT_QUOTES, 'UTF-8')));
  136  		} else {

  140  		if (isset($this->request->get['path'])) {
  141: 			$path = preg_replace('[^a-zA-z0-9_\:\/]', '', html_entity_decode(trim($this->request->get['path']), ENT_QUOTES, 'UTF-8'));
  142  		} else {

  284  		if (isset($this->request->get['name'])) {
  285: 			$name = preg_replace('[^a-zA-z0-9]', '', basename(html_entity_decode(trim((string)$this->request->get['name']), ENT_QUOTES, 'UTF-8')));
  286  		} else {

admin/controller/customer/custom_field.php:
  386  
  387: 		if ($this->request->post['type'] == 'text' && $this->request->post['validation'] && @preg_match(html_entity_decode($this->request->post['validation'], ENT_QUOTES, 'UTF-8'), null) === false) {
  388  			$json['error']['validation'] = $this->language->get('error_validation');

admin/controller/customer/customer.php:
  692  					$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  693: 				} elseif (($custom_field['location'] == 'account') && ($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['custom_field'][$custom_field['custom_field_id']])) {
  694  					$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

  747  							$json['error']['address_' . $key . '_custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  748: 						} elseif (($custom_field['location'] == 'address') && ($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $value['custom_field'][$custom_field['custom_field_id']])) {
  749  							$json['error']['address_' . $key . '_custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

admin/controller/design/seo_url.php:
  515  
  516: 			if (preg_match('/[^a-zA-Z0-9\/_-]|[\p{Cyrillic}]+/u', $keyword)) {
  517  				$json['error']['keyword'] = $this->language->get('error_keyword_character');

admin/controller/marketing/affiliate.php:
  759  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  760: 					} elseif (($custom_field['location'] == 'affiliate') && ($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['custom_field'][$custom_field['custom_field_id']])) {
  761  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

admin/controller/sale/order.php:
  1397  
  1398: 				$payment_address = str_replace(["\r\n", "\r", "\n"], '<br/>', preg_replace(["/\s\s+/", "/\r\r+/", "/\n\n+/"], '<br/>', trim(str_replace($find, $replace, $format))));
  1399  

  1432  
  1433: 				$shipping_address = str_replace(["\r\n", "\r", "\n"], '<br/>', preg_replace(["/\s\s+/", "/\r\r+/", "/\n\n+/"], '<br/>', trim(str_replace($find, $replace, $format))));
  1434  

  1643  
  1644: 				$shipping_address = str_replace(["\r\n", "\r", "\n"], '<br/>', preg_replace(["/\s\s+/", "/\r\r+/", "/\n\n+/"], '<br/>', trim(str_replace($find, $replace, $format))));
  1645  

admin/controller/setting/setting.php:
  817  			$json['error']['error_filename'] = $this->language->get('error_log_required');
  818: 		} elseif (preg_match('/\.\.[\/\\\]?/', $this->request->post['config_error_filename'])) {
  819  			$json['error']['error_filename'] = $this->language->get('error_log_invalid');

admin/controller/tool/backup.php:
  196  
  197: 				$output .= 'INSERT INTO `' . $table . '` (' . preg_replace('/, $/', '', $fields) . ') VALUES (' . preg_replace('/, $/', '', $values) . ');' . "\n";
  198  			}

admin/controller/tool/upload.php:
  362  
  363: 			$extension_allowed = preg_replace('~\r?\n~', "\n", $this->config->get('config_file_ext_allowed'));
  364  

  377  
  378: 			$mime_allowed = preg_replace('~\r?\n~', "\n", $this->config->get('config_file_mime_allowed'));
  379  

catalog/controller/account/address.php:
  118  				'address_id' => $result['address_id'],
  119: 				'address'    => str_replace(["\r\n", "\r", "\n"], '<br/>', preg_replace(["/\s\s+/", "/\r\r+/", "/\n\n+/"], '<br/>', trim(str_replace($find, $replace, $result['address_format'])))),
  120  				'edit'       => $this->url->link('account/address.form', 'language=' . $this->config->get('config_language') . '&customer_token=' . $this->session->data['customer_token'] . '&address_id=' . $result['address_id']),

  360  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  361: 					} elseif (($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['custom_field'][$custom_field['custom_field_id']])) {
  362  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

catalog/controller/account/affiliate.php:
  227  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  228: 					} elseif (($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['custom_field'][$custom_field['custom_field_id']])) {
  229  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

catalog/controller/account/edit.php:
  149  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  150: 					} elseif (($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['custom_field'][$custom_field['custom_field_id']])) {
  151  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

catalog/controller/account/order.php:
  216  
  217: 			$data['payment_address'] = str_replace(["\r\n", "\r", "\n"], '<br/>', preg_replace(["/\s\s+/", "/\r\r+/", "/\n\n+/"], '<br/>', trim(str_replace($find, $replace, $format))));
  218  

  254  
  255: 				$data['shipping_address'] = str_replace(["\r\n", "\r", "\n"], '<br/>', preg_replace(["/\s\s+/", "/\r\r+/", "/\n\n+/"], '<br/>', trim(str_replace($find, $replace, $format))));
  256  

catalog/controller/account/register.php:
  189  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  190: 					} elseif (($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['custom_field'][$custom_field['custom_field_id']])) {
  191  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

catalog/controller/account/subscription.php:
  257  
  258: 				$data['payment_address'] = str_replace(["\r\n", "\r", "\n"], '<br/>', preg_replace(["/\s\s+/", "/\r\r+/", "/\n\n+/"], '<br/>', trim(str_replace($find, $replace, $format))));
  259  			} else {

  306  
  307: 				$data['shipping_address'] = str_replace(["\r\n", "\r", "\n"], '<br/>', preg_replace(["/\s\s+/", "/\r\r+/", "/\n\n+/"], '<br/>', trim(str_replace($find, $replace, $format))));
  308  			} else {

catalog/controller/api/sale/customer.php:
  82  					$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  83: 				} elseif (($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['custom_field'][$custom_field['custom_field_id']])) {
  84  					$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

catalog/controller/api/sale/payment_address.php:
  76  					$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  77: 				} elseif (($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['custom_field'][$custom_field['custom_field_id']])) {
  78  					$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

catalog/controller/api/sale/shipping_address.php:
  77  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  78: 					} elseif (($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['custom_field'][$custom_field['custom_field_id']])) {
  79  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

catalog/controller/checkout/payment_address.php:
  146  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  147: 					} elseif (($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['custom_field'][$custom_field['custom_field_id']])) {
  148  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

catalog/controller/checkout/register.php:
  292  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  293: 					} elseif (($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['custom_field'][$custom_field['location']][$custom_field['custom_field_id']])) {
  294  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

  328  							$json['error']['payment_custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  329: 						} elseif (($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['payment_custom_field'][$custom_field['location']][$custom_field['custom_field_id']])) {
  330  							$json['error']['payment_custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

  376  							$json['error']['shipping_custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  377: 						} elseif (($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['shipping_custom_field'][$custom_field['location']][$custom_field['custom_field_id']])) {
  378  							$json['error']['shipping_custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

catalog/controller/checkout/shipping_address.php:
  157  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_custom_field'), $custom_field['name']);
  158: 					} elseif (($custom_field['type'] == 'text') && !empty($custom_field['validation']) && !preg_match(html_entity_decode($custom_field['validation'], ENT_QUOTES, 'UTF-8'), $this->request->post['custom_field'][$custom_field['custom_field_id']])) {
  159  						$json['error']['custom_field_' . $custom_field['custom_field_id']] = sprintf($this->language->get('error_regex'), $custom_field['name']);

catalog/controller/mail/order.php:
  202  
  203: 		$data['payment_address'] = str_replace(["\r\n", "\r", "\n"], '<br/>', preg_replace(["/\s\s+/", "/\r\r+/", "/\n\n+/"], '<br/>', trim(str_replace($find, $replace, $format))));
  204  

  237  
  238: 		$data['shipping_address'] = str_replace(["\r\n", "\r", "\n"], '<br/>', preg_replace(["/\s\s+/", "/\r\r+/", "/\n\n+/"], '<br/>', trim(str_replace($find, $replace, $format))));
  239  

catalog/controller/tool/upload.php:
  18  			// Sanitize the filename
  19: 			$filename = basename(preg_replace('/[^a-zA-Z0-9\.\-\s+]/', '', html_entity_decode($this->request->files['file']['name'], ENT_QUOTES, 'UTF-8')));
  20  

  28  
  29: 			$extension_allowed = preg_replace('~\r?\n~', "\n", $this->config->get('config_file_ext_allowed'));
  30  

  43  
  44: 			$mime_allowed = preg_replace('~\r?\n~', "\n", $this->config->get('config_file_mime_allowed'));
  45  

catalog/model/catalog/product.php:
  105  
  106: 				$words = explode(' ', trim(preg_replace('/\s+/', ' ', $data['filter_search'])));
  107  

  127  
  128: 				$words = explode(' ', trim(preg_replace('/\s+/', ' ', $data['filter_tag'])));
  129  

  434  
  435: 				$words = explode(' ', trim(preg_replace('/\s+/', ' ', $data['filter_search'])));
  436  

  456  
  457: 				$words = explode(' ', trim(preg_replace('/\s+/', ' ', $data['filter_tag'])));
  458  

catalog/model/cms/article.php:
   42  
   43: 			$words = explode(' ', trim(preg_replace('/\s+/', ' ', $data['filter_search'])));
   44  

  113  
  114: 			$words = explode(' ', trim(preg_replace('/\s+/', ' ', $data['filter_search'])));
  115  

install/controller/install/step_3.php:
  306  
  307: 		if ($this->request->post['db_prefix'] && preg_match('/[^a-z0-9_]/', $this->request->post['db_prefix'])) {
  308  			$this->error['db_prefix'] = $this->language->get('error_db_prefix');

install/controller/startup/database.php:
  19  			foreach ($lines as $number => $line) {
  20: 				if (strpos(strtoupper($line), 'DB_') !== false && preg_match('/define\(\'(.*)\',\s+\'(.*)\'\)/', $line, $match, PREG_OFFSET_CAPTURE)) {
  21  					define($match[1][0], $match[2][0]);

install/controller/upgrade/upgrade_1.php:
   39  			foreach ($lines as $number => $line) {
   40: 				if (preg_match('/define\(\'(.*)\',\s+\'(.*)\'\)/', $line, $match, PREG_OFFSET_CAPTURE)) {
   41  					$config[$match[1][0]] = $match[2][0];

  151  			foreach ($lines as $number => $line) {
  152: 				if (preg_match('/define\(\'(.*)\',\s+\'(.*)\'\)/', $line, $match, PREG_OFFSET_CAPTURE)) {
  153  					$config[$match[1][0]] = $match[2][0];

install/controller/upgrade/upgrade_2.php:
  40  		foreach ($lines as $number => $line) {
  41: 			if (preg_match('/define\(\'(.*)\',\s+\'(.*)\'\)/', $line, $match, PREG_OFFSET_CAPTURE)) {
  42  				$config[$match[1][0]] = $match[2][0];

install/controller/upgrade/upgrade_4.php:
  32  			foreach ($query->rows as $result) {
  33: 				if (preg_match('/^(a:)/', $result['value'])) {
  34  					$this->db->query("UPDATE `" . DB_PREFIX . "setting` SET `value` = '" . $this->db->escape(json_encode(unserialize($result['value']))) . "' WHERE `setting_id` = '" . (int)$result['setting_id'] . "'");

install/controller/upgrade/upgrade_6.php:
  22  			foreach ($query->rows as $result) {
  23: 				if (preg_match('/^(a:)/', $result['custom_field'])) {
  24  					$this->db->query("UPDATE `" . DB_PREFIX . "customer` SET `custom_field` = '" . $this->db->escape(json_encode(unserialize($result['custom_field']))) . "' WHERE `customer_id` = '" . (int)$result['customer_id'] . "'");

  31  			foreach ($query->rows as $result) {
  32: 				if (preg_match('/^(a:)/', $result['data'])) {
  33  					$this->db->query("UPDATE `" . DB_PREFIX . "customer_activity` SET `data` = '" . $this->db->escape(json_encode(unserialize($result['data']))) . "' WHERE `customer_activity_id` = '" . (int)$result['customer_activity_id'] . "'");

  40  			foreach ($query->rows as $result) {
  41: 				if (preg_match('/^(a:)/', $result['custom_field'])) {
  42  					$this->db->query("UPDATE `" . DB_PREFIX . "address` SET `custom_field` = '" . $this->db->escape(json_encode(unserialize($result['custom_field']))) . "' WHERE `address_id` = '" . (int)$result['address_id'] . "'");

  49  			foreach ($query->rows as $result) {
  50: 				if (preg_match('/^(a:)/', $result['setting'])) {
  51  					$this->db->query("UPDATE `" . DB_PREFIX . "module` SET `setting` = '" . $this->db->escape(json_encode(unserialize($result['setting']))) . "' WHERE `module_id` = '" . (int)$result['module_id'] . "'");

  58  			foreach ($query->rows as $result) {
  59: 				if (preg_match('/^(a:)/', $result['custom_field'])) {
  60  					$this->db->query("UPDATE `" . DB_PREFIX . "order` SET `custom_field` = '" . $this->db->escape(json_encode(unserialize($result['custom_field']))) . "' WHERE `order_id` = '" . (int)$result['order_id'] . "'");

  62  
  63: 				if (preg_match('/^(a:)/', $result['payment_custom_field'])) {
  64  					$this->db->query("UPDATE `" . DB_PREFIX . "order` SET `payment_custom_field` = '" . $this->db->escape(json_encode(unserialize($result['payment_custom_field']))) . "' WHERE `order_id` = '" . (int)$result['order_id'] . "'");

  66  
  67: 				if (preg_match('/^(a:)/', $result['shipping_custom_field'])) {
  68  					$this->db->query("UPDATE `" . DB_PREFIX . "order` SET `shipping_custom_field` = '" . $this->db->escape(json_encode(unserialize($result['shipping_custom_field']))) . "' WHERE `order_id` = '" . (int)$result['order_id'] . "'");

  75  			foreach ($query->rows as $result) {
  76: 				if (preg_match('/^(a:)/', $result['permission'])) {
  77  					$this->db->query("UPDATE `" . DB_PREFIX . "user_group` SET `permission` = '" . $this->db->escape(json_encode(unserialize($result['permission']))) . "' WHERE `user_group_id` = '" . (int)$result['user_group_id'] . "'");

system/engine/action.php:
  32  	public function __construct(string $route) {
  33: 		$this->route = preg_replace('/[^a-zA-Z0-9_|\/\.]/', '', $route);
  34  

system/engine/autoloader.php:
  65  				if (!$this->path[$namespace]['psr4']) {
  66: 					$file = $this->path[$namespace]['directory'] . trim(str_replace('\\', '/', strtolower(preg_replace('~([a-z])([A-Z]|[0-9])~', '\\1_\\2', substr($class, strlen($namespace))))), '/') . '.php';
  67  				} else {

system/engine/event.php:
  64  		foreach ($this->data as $value) {
  65: 			if (preg_match('/^' . str_replace(['\*', '\?'], ['.*', '.'], preg_quote($value['trigger'], '/')) . '/', $event)) {
  66  				$result = $value['action']->execute($this->registry, $args);

system/engine/loader.php:
   66  		// Sanitize the call
   67: 		$route = preg_replace('/[^a-zA-Z0-9_|\/\.]/', '', str_replace('|', '.', $route));
   68  

  119  		// Sanitize the call
  120: 		$route = preg_replace('/[^a-zA-Z0-9_\/]/', '', $route);
  121  

  194  		// Sanitize the call
  195: 		$route = preg_replace('/[^a-zA-Z0-9_\/]/', '', $route);
  196  

  231  		// Sanitize the call
  232: 		$route = preg_replace('/[^a-zA-Z0-9_\-\/]/', '', $route);
  233  

  265  		// Sanitize the call
  266: 		$route = preg_replace('/[^a-zA-Z0-9_\-\/]/', '', $route);
  267  

  298  	public function helper(string $route): void {
  299: 		$route = preg_replace('/[^a-zA-Z0-9_\/]/', '', $route);
  300  

system/helper/bbcode.php:
  66  
  67: 	$string = preg_replace($pattern, $replace, $string);
  68  

system/library/session.php:
  76  
  77: 		if (preg_match('/^[a-zA-Z0-9,\-]{22,52}$/', $session_id)) {
  78  			$this->session_id = $session_id;

system/library/cache/file.php:
  30  	public function get(string $key): array|string|null {
  31: 		$files = glob(DIR_CACHE . 'cache.' . preg_replace('/[^A-Z0-9\._-]/i', '', $key) . '.*');
  32  

  54  
  55: 		file_put_contents(DIR_CACHE . 'cache.' . preg_replace('/[^A-Z0-9\._-]/i', '', $key) . '.' . (time() + $expire), json_encode($value));
  56  	}

  65  	public function delete(string $key): void {
  66: 		$files = glob(DIR_CACHE . 'cache.' . preg_replace('/[^A-Z0-9\._-]/i', '', $key) . '.*');
  67  

system/library/db/pdo.php:
  60  	public function query(string $sql): bool|object {
  61: 		$sql = preg_replace('/(?:\'\:)([a-z0-9]*.)(?:\')/', ':$1', $sql);
  62  

system/storage/vendor/aws/aws-crt-php/gen_api.php:
  10      // Strip AWS_EXTERN_C_BEGIN/END
  11:     if (preg_match('/AWS_EXTERN_C/', $line)) {
  12          continue;

  15      // Strip macros/includes
  16:     if (preg_match('/^#/', $line)) {
  17          continue;

system/storage/vendor/aws/aws-crt-php/gen_stub.php:
    29          $pathName = $file->getPathName();
    30:         if (preg_match('/\.stub\.php$/', $pathName)) {
    31              $fileInfo = processStubFile($pathName, $context);

    91      $arginfoCode = file_get_contents($arginfoFile);
    92:     if (!preg_match('/\* Stub hash: ([0-9a-f]+) \*/', $arginfoCode, $matches)) {
    93          return null;

   933                      $initializer = $doc->createElement('initializer');
   934:                     if (preg_match('/^[a-zA-Z_][a-zA-Z_0-9]*$/', $defaultValue)) {
   935                          $constant = $doc->createElement('constant', $defaultValue);

  1033          if ($this->name === "param") {
  1034:             preg_match('/^\s*([\w\|\\\\\[\]]+)\s*\$\w+.*$/', $value, $matches);
  1035          } elseif ($this->name === "return") {
  1036:             preg_match('/^\s*([\w\|\\\\\[\]]+)\s*$/', $value, $matches);
  1037          }

  1054          if ($this->name === "param") {
  1055:             preg_match('/^\s*[\w\|\\\\\[\]]+\s*\$(\w+).*$/', $value, $matches);
  1056          } elseif ($this->name === "prefer-ref") {
  1057:             preg_match('/^\s*\$(\w+).*$/', $value, $matches);
  1058          }

  1073          $regex = '/^\*\s*@([a-z-]+)(?:\s+(.+))?$/';
  1074:         if (preg_match($regex, trim($commentLine), $matches)) {
  1075              $tags[] = new DocCommentTag($matches[1], $matches[2] ?? null);

  1217          $text = trim($comment->getText());
  1218:         if (preg_match('/^#\s*if\s+(.+)$/', $text, $matches)) {
  1219              $conds[] = $matches[1];
  1220:         } else if (preg_match('/^#\s*ifdef\s+(.+)$/', $text, $matches)) {
  1221              $conds[] = "defined($matches[1])";
  1222:         } else if (preg_match('/^#\s*ifndef\s+(.+)$/', $text, $matches)) {
  1223              $conds[] = "!defined($matches[1])";
  1224:         } else if (preg_match('/^#\s*else$/', $text)) {
  1225              if (empty($conds)) {

  1229              $conds[] = "!($cond)";
  1230:         } else if (preg_match('/^#\s*endif$/', $text)) {
  1231              if (empty($conds)) {

  1606          $pathName = $file->getPathName();
  1607:         if (!preg_match('/\.xml$/i', $pathName)) {
  1608              continue;

  1619  
  1620:         $replacedXml = preg_replace("/&([A-Za-z0-9._{}%-]+?;)/", "REPLACED-ENTITY-$1", $xml);
  1621  

  1699              $xml1 = $doc->saveXML($methodSynopsis);
  1700:             $xml1 = preg_replace("/&([A-Za-z0-9._{}%-]+?;)/", "REPLACED-ENTITY-$1", $xml1);
  1701              $docComparator->loadXML($xml1);

  1706              $xml2 = $doc->saveXML($newMethodSynopsis);
  1707:             $xml2 = preg_replace("/&([A-Za-z0-9._{}%-]+?;)/", "REPLACED-ENTITY-$1", $xml2);
  1708              $docComparator->loadXML($xml2);

system/storage/vendor/aws/aws-sdk-php/src/functions.php:
  428      return (
  429:         preg_match("/^([a-z\d](-*[a-z\d])*)(\.([a-z\d](-*[a-z\d])*))*\.?$/i", $hostname)
  430:         && preg_match("/^.{1,253}$/", $hostname)
  431:         && preg_match("/^[^\.]{1,63}(\.[^\.]{0,63})*$/", $hostname)
  432      );

  442  {
  443:     return preg_match("/^(?!-)[a-zA-Z0-9-]{1,63}(?<!-)$/", $label);
  444  }

  460      return parse_ini_string(
  461:         preg_replace('/^#.*\\n/m', "", file_get_contents($filename)),
  462          $process_sections,

  514      if (is_string($input) || is_numeric($input)) {
  515:         if (is_string($input) && !preg_match("/^-?[0-9]+\.?[0-9]*$/", $input)) {
  516              return false;

system/storage/vendor/aws/aws-sdk-php/src/TraceMiddleware.php:
  57       *   expressions to scrubbed strings. These mappings are passed directly to
  58:      *   preg_replace (e.g., preg_replace($key, $value, $debugOutput) if
  59       *   "scrub_auth" is set to true.

system/storage/vendor/aws/aws-sdk-php/src/Api/Validator.php:
  222              $pattern = $shape['pattern'];
  223:             if ($pattern && !preg_match("/$pattern/", $value)) {
  224                  $this->addError("Pattern /$pattern/ failed to match '$value'");

system/storage/vendor/aws/aws-sdk-php/src/Arn/Arn.php:
  182          }
  183:         if ($value = preg_match("/^[a-zA-Z0-9-]+$/", $string)) {
  184              return true;

system/storage/vendor/aws/aws-sdk-php/src/CloudFront/Signer.php:
  77          if ($policy) {
  78:             $policy = preg_replace('/\s/s', '', $policy);
  79              $signatureHash['Policy'] = $this->encode($policy);

system/storage/vendor/aws/aws-sdk-php/src/CloudTrail/LogFileIterator.php:
  286                      function ($object) use ($regex) {
  287:                         return preg_match("#{$regex}#", $object['Key']);
  288                      }

  311              $fn = function ($object) use ($startDate, $endDate) {
  312:                 if (!preg_match('/[0-9]{8}T[0-9]{4}Z/', $object['Key'], $m)) {
  313                      return false;

system/storage/vendor/aws/aws-sdk-php/src/Credentials/AssumeRoleWithWebIdentityCredentialProvider.php:
  61  
  62:         if (!preg_match("/^\w\:|^\/|^\\\/", $this->tokenFile)) {
  63              throw new \InvalidArgumentException("'WebIdentityTokenFile' must be an absolute path.");

system/storage/vendor/aws/aws-sdk-php/src/EventBridge/EventBridgeEndpointMiddleware.php:
  86          }
  87:         if ($value = preg_match("/^[a-zA-Z0-9-.]+$/", $string)) {
  88              return true;

system/storage/vendor/aws/aws-sdk-php/src/S3/GetBucketLocationParser.php:
  32              $location = 'us-east-1';
  33:             if (preg_match('/>(.+?)<\/LocationConstraint>/', $response->getBody(), $matches)) {
  34                  $location = $matches[1] === 'EU' ? 'eu-west-1' : $matches[1];

system/storage/vendor/aws/aws-sdk-php/src/S3/S3Client.php:
  436              !filter_var($bucket, FILTER_VALIDATE_IP) &&
  437:             preg_match('/^[a-z0-9]([a-z0-9\-\.]*[a-z0-9])?$/', $bucket);
  438      }

system/storage/vendor/aws/aws-sdk-php/src/S3/S3ClientTrait.php:
  147              $iter = \Aws\filter($iter, function ($c) use ($regex) {
  148:                 return preg_match($regex, $c['Key']);
  149              });

system/storage/vendor/aws/aws-sdk-php/src/S3/S3EndpointMiddleware.php:
  287          $pattern = '/^\\/' . preg_quote($command['Bucket'], '/') . '/';
  288:         $path = preg_replace($pattern, '', $path) ?: '/';
  289          if (substr($path, 0 , 1) !== '/') {

system/storage/vendor/aws/aws-sdk-php/src/S3/S3UriParser.php:
  65  
  66:         if (!preg_match($this->pattern, $url->getHost(), $matches)) {
  67              return $this->parseCustomEndpoint($url);

  82      {
  83:         preg_match("/^([a-zA-Z0-9]*):\/\/([a-zA-Z0-9:-]*)\/(.*)/", $uri, $components);
  84          if (empty($components)) {

system/storage/vendor/aws/aws-sdk-php/src/S3/Transfer.php:
  253              // Prepare the sink.
  254:             $objectKey = preg_replace('/^' . preg_quote($prefix, '/') . '/', '', $object);
  255              $sink = $this->destination['path'] . '/' . $objectKey;

  370          $relative_file_path = ltrim(
  371:             preg_replace('#^' . preg_quote($this->sourceMetadata['path']) . '#', '', $filename),
  372              '/\\'

system/storage/vendor/aws/aws-sdk-php/src/Signature/SignatureV4.php:
  320              }
  321:             $canonHeaders[] = $k . ':' . preg_replace('/\s+/', ' ', implode(',', $v));
  322          }

system/storage/vendor/bin/jp.php:
  45                  if ($this->position === 0) {
  46:                     $data = preg_replace('{^#!.*\r?\n}', '', $data);
  47                  }

system/storage/vendor/bin/pscss:
  45                  if ($this->position === 0) {
  46:                     $data = preg_replace('{^#!.*\r?\n}', '', $data);
  47                  }

system/storage/vendor/guzzlehttp/guzzle/src/Cookie/SetCookie.php:
  396  
  397:         return (bool) \preg_match('/\.' . \preg_quote($cookieDomain, '/') . '$/', $domain);
  398      }

system/storage/vendor/guzzlehttp/guzzle/src/Handler/CurlFactory.php:
  464              $ext = pathinfo($cert, \PATHINFO_EXTENSION);
  465:             if (preg_match('#^(der|p12)$#i', $ext)) {
  466                  $conf[\CURLOPT_SSLCERTTYPE] = strtoupper($ext);

system/storage/vendor/guzzlehttp/psr7/src/Message.php:
   79          // letters, marks, numbers, punctuation, spacing, and separators.
   80:         if (preg_match('/[^\pL\pM\pN\pP\pS\pZ\n\r\t]/u', $summary)) {
   81              return null;

  138  
  139:         if (preg_match("/(?:^HTTP\/|^[A-Z]+ \S+ HTTP\/)(\d+(?:\.\d+)?)/i", $startLine, $matches) && $matches[1] === '1.0') {
  140              // Header folding is deprecated for HTTP/1.1, but allowed in HTTP/1.0
  141:             $rawHeaders = preg_replace(Rfc7230::HEADER_FOLD_REGEX, ' ', $rawHeaders);
  142          }

  149              // Folding is deprecated, see https://tools.ietf.org/html/rfc7230#section-3.2.4
  150:             if (preg_match(Rfc7230::HEADER_FOLD_REGEX, $rawHeaders)) {
  151                  throw new \InvalidArgumentException('Invalid header syntax: Obsolete line folding');

  204          $matches = [];
  205:         if (!preg_match('/^[\S]+\s+([a-zA-Z]+:\/\/|\/).*/', $data['start-line'], $matches)) {
  206              throw new \InvalidArgumentException('Invalid request string');

  232          // responses without space and reason as well.
  233:         if (!preg_match('/^HTTP\/.* [0-9]{3}( .*|$)/', $data['start-line'])) {
  234              throw new \InvalidArgumentException('Invalid response string: ' . $data['start-line']);

system/storage/vendor/guzzlehttp/psr7/src/MessageTrait.php:
  226  
  227:         if (! preg_match('/^[a-zA-Z0-9\'`#$%&*+.^_|~!-]+$/', $header)) {
  228              throw new \InvalidArgumentException(

  259          // folding is not likely to break any legitimate use case.
  260:         if (! preg_match('/^[\x20\x09\x21-\x7E\x80-\xFF]*$/', $value)) {
  261              throw new \InvalidArgumentException(sprintf('"%s" is not valid header value', $value));

system/storage/vendor/guzzlehttp/psr7/src/Request.php:
  79      {
  80:         if (preg_match('#\s#', $requestTarget)) {
  81              throw new InvalidArgumentException(

system/storage/vendor/guzzlehttp/psr7/src/Stream.php:
  63          $this->seekable = $meta['seekable'];
  64:         $this->readable = (bool)preg_match(self::READABLE_MODES, $meta['mode']);
  65:         $this->writable = (bool)preg_match(self::WRITABLE_MODES, $meta['mode']);
  66          $this->uri = $this->getMetadata('uri');

system/storage/vendor/guzzlehttp/psr7/src/Uri.php:
  108          $prefix = '';
  109:         if (preg_match('%^(.*://\[[0-9:a-f]+\])(.*?)$%', $url, $matches)) {
  110              /** @var array{0:string, 1:string, 2:string} $matches */

system/storage/vendor/guzzlehttp/psr7/src/UriNormalizer.php:
  152          if ($flags & self::REMOVE_DUPLICATE_SLASHES) {
  153:             $uri = $uri->withPath(preg_replace('#//++#', '/', $uri->getPath()));
  154          }

system/storage/vendor/scssphp/scssphp/bin/pscss:
  49  
  50:     if (! preg_match('/^(?:' . implode('|', (array) $options) . ')=?(.*)/', $argv[$i], $matches)) {
  51          return;

system/storage/vendor/scssphp/scssphp/src/Compiler.php:
   1018              strpos($part, ':') === 0 &&
   1019:             preg_match(",^::?([\w-]+)\((.+)\)$,", $part, $matches)
   1020          ) {

   1096  
   1097:             if (! preg_match('/^[\[.:#%]/', $part) && \count($single)) {
   1098                  $single[\count($single) - 1] .= $part;

   1107              $matches = null;
   1108:             $extendingDecoratedTag = preg_match('/^[a-z0-9]+$/i', $single[0], $matches) ? $matches[0] : false;
   1109          }

   1177                      $extendingDecoratedTag && $replacement[0] != $extendingDecoratedTag &&
   1178:                     preg_match('/^[a-z0-9]+$/i', $replacement[0])
   1179                  ) {

   1255              foreach ($single as $part) {
   1256:                 if (preg_match('/^[\[:]/', $part)) {
   1257                      $out[] = $part;
   1258                      $wasTag = false;
   1259:                 } elseif (preg_match('/^[\.#]/', $part)) {
   1260                      array_unshift($out, $part);
   1261                      $wasTag = false;
   1262:                 } elseif (preg_match('/^[^_-]/', $part) && $rang === 1) {
   1263                      $tag[] = $part;

   1716                      return $this->testWithWithout($this->compileDirectiveName($block->name), $with, $without);
   1717:                 } elseif (isset($block->selectors) && preg_match(',@(\w+),ims', json_encode($block->selectors), $m)) {
   1718                      return $this->testWithWithout($m[1], $with, $without);

   2060                  // force re-evaluation if self char or non standard char
   2061:                 if (preg_match(',[^\w-],', $p)) {
   2062                      $this->shouldEvaluate = true;

   2201                  ! \is_string($part) ||
   2202:                 preg_match('/[\[.:#%]/', $part)
   2203              ) {

   3915                  if ($actualLibName !== $libName || strtolower($normalizedName) !== $normalizedName) {
   3916:                     $kebabCaseName = preg_replace('~(?<=\\w)([A-Z])~', '-$1', substr($actualLibName, 3));
   3917                      assert($kebabCaseName !== null);

   5779      {
   5780:         return 1 === preg_match('~\.css$|^https?://|^//~', $url);
   5781      }

   5880  
   5881:         $hasExtension = preg_match('/.s[ac]ss$/', $url);
   5882  

   7173                  // hexa color?
   7174:                 if (preg_match('/^#([0-9a-f]+)$/i', $name, $m)) {
   7175                      $nofValues = \strlen($m[1]);

  10378          foreach ($parts as $part) {
  10379:             if (! preg_match('/^[\[.:#%_-]/', $part)) {
  10380                  return $part;

system/storage/vendor/scssphp/scssphp/src/Parser.php:
  1222          $r = '/' . $regex . '/' . $this->patternModifiers;
  1223:         $result = preg_match($r, $this->buffer, $out, 0, $from);
  1224  

  1507  
  1508:         if (! preg_match($r, $this->buffer, $out, 0, $this->count)) {
  1509              return false;

  1594  
  1595:         while (preg_match(static::$whitePattern, $this->buffer, $m, 0, $this->count)) {
  1596              if (isset($m[1]) && empty($this->commentsSeen[$this->count])) {

  2799  
  2800:             if ($name !== 'expression' && ! preg_match('/^(-[a-z]+-)?calc$/', $name)) {
  2801                  $ss = $this->count;

  3327                  if ($lookWhite) {
  3328:                     $left = ($s > 0 && preg_match('/\s/', $this->buffer[$s - 1])) ? ' ' : '';
  3329                      $right = (
  3330                          ! empty($this->buffer[$this->count]) &&
  3331:                         preg_match('/\s/', $this->buffer[$this->count])
  3332                      ) ? ' ' : '';

  3398          // match comment hack
  3399:         if (preg_match(static::$whitePattern, $this->buffer, $m, 0, $this->count)) {
  3400              if (! empty($m[0])) {

  3583              if (strlen($escapedout) === 1) {
  3584:                 if (!preg_match(",\w,", $escapedout)) {
  3585                      $out = '\\' . $escapedout;

system/storage/vendor/scssphp/scssphp/src/Formatter/Expanded.php:
  59              if (substr($line, 0, 2) === '/*') {
  60:                 $replacedLine = preg_replace('/\r\n?|\n|\f/', $this->break, $line);
  61                  assert($replacedLine !== null);

system/storage/vendor/scssphp/scssphp/src/Formatter/Nested.php:
  70              if (substr($line, 0, 2) === '/*') {
  71:                 $replacedLine = preg_replace('/\r\n?|\n|\f/', $this->break, $line);
  72                  assert($replacedLine !== null);

system/storage/vendor/scssphp/scssphp/src/Util/Path.php:
  44  
  45:         if (!preg_match('/^[A-Za-z]$/', $path[0])) {
  46              return false;

system/storage/vendor/symfony/polyfill-ctype/Ctype.php:
   35  
   36:         return \is_string($text) && '' !== $text && !preg_match('/[^A-Za-z0-9]/', $text);
   37      }

   51  
   52:         return \is_string($text) && '' !== $text && !preg_match('/[^A-Za-z]/', $text);
   53      }

   67  
   68:         return \is_string($text) && '' !== $text && !preg_match('/[^\x00-\x1f\x7f]/', $text);
   69      }

   83  
   84:         return \is_string($text) && '' !== $text && !preg_match('/[^0-9]/', $text);
   85      }

   99  
  100:         return \is_string($text) && '' !== $text && !preg_match('/[^!-~]/', $text);
  101      }

  115  
  116:         return \is_string($text) && '' !== $text && !preg_match('/[^a-z]/', $text);
  117      }

  131  
  132:         return \is_string($text) && '' !== $text && !preg_match('/[^ -~]/', $text);
  133      }

  147  
  148:         return \is_string($text) && '' !== $text && !preg_match('/[^!-\/\:-@\[-`\{-~]/', $text);
  149      }

  163  
  164:         return \is_string($text) && '' !== $text && !preg_match('/[^\s]/', $text);
  165      }

  179  
  180:         return \is_string($text) && '' !== $text && !preg_match('/[^A-Z]/', $text);
  181      }

  195  
  196:         return \is_string($text) && '' !== $text && !preg_match('/[^A-Fa-f0-9]/', $text);
  197      }

system/storage/vendor/symfony/polyfill-mbstring/Mbstring.php:
  167              $encoding = null;
  168:             if (!preg_match('//u', $s)) {
  169                  $s = @\iconv('UTF-8', 'UTF-8//IGNORE', $s);

  233              $encoding = null;
  234:             if (!preg_match('//u', $s)) {
  235                  $s = @\iconv('UTF-8', 'UTF-8//IGNORE', $s);

  281              $encoding = null;
  282:             if (!preg_match('//u', $s)) {
  283                  $s = @\iconv('UTF-8', 'UTF-8//IGNORE', $s);

  432                  case 'ASCII':
  433:                     if (!preg_match('/[\x80-\xFF]/', $str)) {
  434                          return $enc;

  439                  case 'UTF-8':
  440:                     if (preg_match('//u', $str)) {
  441                          return 'UTF-8';

  741  
  742:         $s = preg_replace('/[\x{1100}-\x{115F}\x{2329}\x{232A}\x{2E80}-\x{303E}\x{3040}-\x{A4CF}\x{AC00}-\x{D7A3}\x{F900}-\x{FAFF}\x{FE10}-\x{FE19}\x{FE30}-\x{FE6F}\x{FF00}-\x{FF60}\x{FFE0}-\x{FFE6}\x{20000}-\x{2FFFD}\x{30000}-\x{3FFFD}]/u', '', $s, -1, $wide);
  743  

system/storage/vendor/twig/twig/src/ExpressionParser.php:
  252              case /* Token::OPERATOR_TYPE */ 8:
  253:                 if (preg_match(Lexer::REGEX_NAME, $token->getValue(), $matches) && $matches[0] == $token->getValue()) {
  254                      // in this context, string operators are variable names

  476                  ||
  477:                 (/* Token::OPERATOR_TYPE */ 8 == $token->getType() && preg_match(Lexer::REGEX_NAME, $token->getValue()))
  478              ) {

  649              $token = $this->parser->getCurrentToken();
  650:             if ($stream->test(/* Token::OPERATOR_TYPE */ 8) && preg_match(Lexer::REGEX_NAME, $token->getValue())) {
  651                  // in this context, string operators are variable names

system/storage/vendor/twig/twig/src/ExtensionSet.php:
  163  
  164:             if ($count && preg_match('#^'.$pattern.'$#', $name, $matches)) {
  165                  array_shift($matches);

  219  
  220:             if ($count && preg_match('#^'.$pattern.'$#', $name, $matches)) {
  221                  array_shift($matches);

  369              if ($count) {
  370:                 if (preg_match('#^'.$pattern.'$#', $name, $matches)) {
  371                      array_shift($matches);

system/storage/vendor/twig/twig/src/Lexer.php:
  249                  // raw data?
  250:                 if (preg_match($this->regexes['lex_block_raw'], $this->code, $match, 0, $this->cursor)) {
  251                      $this->moveCursor($match[0]);

  253                  // {% line \d+ %}
  254:                 } elseif (preg_match($this->regexes['lex_block_line'], $this->code, $match, 0, $this->cursor)) {
  255                      $this->moveCursor($match[0]);

  273      {
  274:         if (empty($this->brackets) && preg_match($this->regexes['lex_block'], $this->code, $match, 0, $this->cursor)) {
  275              $this->pushToken(/* Token::BLOCK_END_TYPE */ 3);

  284      {
  285:         if (empty($this->brackets) && preg_match($this->regexes['lex_var'], $this->code, $match, 0, $this->cursor)) {
  286              $this->pushToken(/* Token::VAR_END_TYPE */ 4);

  296          // whitespace
  297:         if (preg_match('/\s+/A', $this->code, $match, 0, $this->cursor)) {
  298              $this->moveCursor($match[0]);

  310          // operators
  311:         elseif (preg_match($this->regexes['operator'], $this->code, $match, 0, $this->cursor)) {
  312:             $this->pushToken(/* Token::OPERATOR_TYPE */ 8, preg_replace('/\s+/', ' ', $match[0]));
  313              $this->moveCursor($match[0]);

  315          // names
  316:         elseif (preg_match(self::REGEX_NAME, $this->code, $match, 0, $this->cursor)) {
  317              $this->pushToken(/* Token::NAME_TYPE */ 5, $match[0]);

  320          // numbers
  321:         elseif (preg_match(self::REGEX_NUMBER, $this->code, $match, 0, $this->cursor)) {
  322              $number = (float) $match[0];  // floats

  350          // strings
  351:         elseif (preg_match(self::REGEX_STRING, $this->code, $match, 0, $this->cursor)) {
  352              $this->pushToken(/* Token::STRING_TYPE */ 7, stripcslashes(substr($match[0], 1, -1)));

  355          // opening double quoted string
  356:         elseif (preg_match(self::REGEX_DQ_STRING_DELIM, $this->code, $match, 0, $this->cursor)) {
  357              $this->brackets[] = ['"', $this->lineno];

  368      {
  369:         if (!preg_match($this->regexes['lex_raw_data'], $this->code, $match, \PREG_OFFSET_CAPTURE, $this->cursor)) {
  370              throw new SyntaxError('Unexpected end of file: Unclosed "verbatim" block.', $this->lineno, $this->source);

  392      {
  393:         if (!preg_match($this->regexes['lex_comment'], $this->code, $match, \PREG_OFFSET_CAPTURE, $this->cursor)) {
  394              throw new SyntaxError('Unclosed comment.', $this->lineno, $this->source);

  401      {
  402:         if (preg_match($this->regexes['interpolation_start'], $this->code, $match, 0, $this->cursor)) {
  403              $this->brackets[] = [$this->options['interpolation'][0], $this->lineno];

  406              $this->pushState(self::STATE_INTERPOLATION);
  407:         } elseif (preg_match(self::REGEX_DQ_STRING_PART, $this->code, $match, 0, $this->cursor) && \strlen($match[0]) > 0) {
  408              $this->pushToken(/* Token::STRING_TYPE */ 7, stripcslashes($match[0]));
  409              $this->moveCursor($match[0]);
  410:         } elseif (preg_match(self::REGEX_DQ_STRING_DELIM, $this->code, $match, 0, $this->cursor)) {
  411              list($expect, $lineno) = array_pop($this->brackets);

  426          $bracket = end($this->brackets);
  427:         if ($this->options['interpolation'][0] === $bracket[0] && preg_match($this->regexes['interpolation_end'], $this->code, $match, 0, $this->cursor)) {
  428              array_pop($this->brackets);

  478              // an operator with a space can be any amount of whitespaces
  479:             $r = preg_replace('/\s+/', '\s+', $r);
  480  

system/storage/vendor/twig/twig/src/Extension/CoreExtension.php:
  1067  {
  1068:     return trim(preg_replace('/>\s+</', '><', $content ?? ''));
  1069  }

system/storage/vendor/twig/twig/src/Extension/EscaperExtension.php:
  253  
  254:             if (!preg_match('//u', $string)) {
  255                  throw new RuntimeError('The string to escape is not a valid UTF-8 string.');

  304  
  305:             if (!preg_match('//u', $string)) {
  306                  throw new RuntimeError('The string to escape is not a valid UTF-8 string.');

  325  
  326:             if (!preg_match('//u', $string)) {
  327                  throw new RuntimeError('The string to escape is not a valid UTF-8 string.');

system/storage/vendor/twig/twig/src/Loader/FilesystemLoader.php:
  231      {
  232:         return preg_replace('#/{2,}#', '/', str_replace('\\', '/', $name));
  233      }

system/storage/vendor/twig/twig/src/Node/Expression/CallExpression.php:
  236      {
  237:         return strtolower(preg_replace(['/([A-Z]+)([A-Z][a-z])/', '/([a-z\d])([A-Z])/'], ['\\1_\\2', '\\1_\\2'], $name));
  238      }

system/storage/vendor/twig/twig/src/Node/Expression/Binary/MatchesBinary.php:
  20          $compiler
  21:             ->raw('preg_match(')
  22              ->subcompile($this->getNode('right'))

system/storage/vendor/twig/twig/src/Test/IntegrationTestCase.php:
   99          foreach (new \RecursiveIteratorIterator(new \RecursiveDirectoryIterator($fixturesDir), \RecursiveIteratorIterator::LEAVES_ONLY) as $file) {
  100:             if (!preg_match('/\.test$/', $file)) {
  101                  continue;

  109  
  110:             if (preg_match('/--TEST--\s*(.*?)\s*(?:--CONDITION--\s*(.*))?\s*(?:--DEPRECATION--\s*(.*?))?\s*((?:--TEMPLATE(?:\(.*?\))?--(?:.*?))+)\s*(?:--DATA--\s*(.*))?\s*--EXCEPTION--\s*(.*)/sx', $test, $match)) {
  111                  $message = $match[1];

  116                  $outputs = [[null, $match[5], null, '']];
  117:             } elseif (preg_match('/--TEST--\s*(.*?)\s*(?:--CONDITION--\s*(.*))?\s*(?:--DEPRECATION--\s*(.*?))?\s*((?:--TEMPLATE(?:\(.*?\))?--(?:.*?))+)--DATA--.*?--EXPECT--.*/s', $test, $match)) {
  118                  $message = $match[1];

```