<?php

// troubleshooting
// error_reporting(E_ALL);
// ini_set('display_errors', '1');

require('rest_processor.php');

if (!empty($article->title)) {
    $articletitle = myPrintTextRunAsReST($article->title);
    } else {
    $articletitle ='title';}

$underline =  str_repeat('=',strlen($articletitle));
  
echo <<<EOT
{$articletitle}
{$underline}


EOT;

myPrintArticleReST($article);

?>