# Code Send SMTP Email from WordPress Without a Plugin

 add_action( 'phpmailer_init', function( $phpmailer ) {
    if ( !is_object( $phpmailer ) )
        $phpmailer = (object) $phpmailer;
    $phpmailer->Mailer     = 'smtp';
    $phpmailer->Host       = 'smtp.gmail.com';
    $phpmailer->SMTPAuth   = true;
    $phpmailer->Port       = 587;
    $phpmailer->Username   = 'arriveddev.bz@gmail.com';
    $phpmailer->Password   = '16 character application password';
    $phpmailer->SMTPSecure = 'TLS';
    $phpmailer->From       = 'arriveddev.bz@gmail.com';
    $phpmailer->FromName   = 'Arriveddev';
});

SOURCE: https://arriveddev.com/send-mail-in-wordpress-without-using-plugin/
