# jquery.hibp.validate

A simple, lightweight jQuery plugin for validating if a password has been previously part of a databreach, using https://haveibeenpwned.com api! - example available on [gh-pages](http://carlwoodhouse.github.com/jquery.hibp.validate)

##### If you like jquery.hibp.validate and use it commercially please consider giving a [donation](https://paypal.me/carlwoodhouse). Thankyou.

## Installation

Include script *after* the jQuery library

    <script src="/path/jquery.hibp.validate.js"></script>

## Example Usage

Check if a password is pwned and throw an alert

	<script type="text/javascript">
        $(function () {
            $('form').on('submit', function () {
                $(':password').hibpValidate();
                return false;
            });

            $(':password').on('hibp', function(event, data) {
                if (data.pwned) {
                    alert('oh dear, your password is one that is compromised according to Troy! pick another ...');
                } else {
                    alert('your password rocks ...')
                }
            });
        }):
	</script>

## Full Example
Check out docs/index.html in the repository or visit our [github-page](https://carlwoodhouse.github.com/jquery.hibp.validate)

  
### Author: [Carl Woodhouse](https://github.com/carlwoodhouse)
Special thanks to [Troy Hunt](https://haveibeenpwned.com) for his awesome api