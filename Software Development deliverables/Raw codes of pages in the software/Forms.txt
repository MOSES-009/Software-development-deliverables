<?php
$dbhost = "localhost";
$dbuser = "root";
$dbpass = "";
$dbname = "services";

$conn = mysqli_connect($dbhost,$dbuser,$dbpass,$dbname);

$month=$_POST['month'];
$day=$_POST['day'];
$year=$_POST['year'];
$medhistory=$_POST['medhistory'];
$area=$_POST['area'];
$medcentre=$_POST['medcentre'];

$sql = "INSERT INTO `medical`( `month`, `day`, `year`, `medhistory`, `area`, `medcentre`) VALUES ('$month','$day','$year','$medhistory','$area','$medcentre')";

$insert = mysqli_query($conn, $sql);
if (!$insert){
echo "Error";
}
else{
echo "You have signed up successfully look for the activation link in your inbox/spam folder of your email account";
}
?>