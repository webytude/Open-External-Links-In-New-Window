#Open External Links In New Window
```php
// ==============================================================================
// A href validation with target blank
// ==============================================================================
function href_target($url = null,$target = null){
 
	if(!empty($url) && $url != null){
		$sit_url = parse_url(get_site_url());
		$link_url = parse_url($url);
		$href = " href='$url'";
	 
		if ($sit_url['host'] !== $link_url['host']){
			$target = (!empty($target)) ? $target : '_blank';
		}
		if(!empty($target)){
			$href .= " target='$target'";
		}
		return $href;
	}
	else{
		return null;
	}
}
```