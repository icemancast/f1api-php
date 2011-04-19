#Changes made to f1 api php library

##Changes made to f1_oauth.php (original file: OAuthClient.php)

line 16: Commented out required since we will autoload in kohana

line 32: Also renamed file name to f1_oauth to follow KO3 convention

line 86:
CHANGED curl_setopt( $this->connection, CURLINFO_HEADER, false ); TO curl_setopt( $this->connection, CURLOPT_HEADER, false );
It was written wrong in original code

line 131: Load config from KO3 config file as opposed to app config

line 219: Commented out below since we are not using appconfig file

line 399: mktime() to time() do to Kohana strict coding

line 450: Commented out since we are not using appconfig file and below is just for debug

##Changes made to f1_signer.php (original file: RequestSigner.php)

File name changed to f1_signer.php to match other file name changes

line 54: getSignatureBaseString() to static method wouldn't load in kohana without doing this

##Changes made to f1_util.php (original file: Util.php)

File name changed to f1_util.php to match other file name changes

line 37: getNormalizedHttpUrl() to static method wouldn't load in kohana without doing this