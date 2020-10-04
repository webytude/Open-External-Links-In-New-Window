#Open External Links In New Window

### once a developer developing a website that faces difficulty for mange continually in every dynamic URLs here is the best function to handle  open third party URLs into the new tab

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