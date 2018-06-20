<html>
<body>
<table style="border:1px #000000 solid;padding:5px;" rules="all" cellpadding='2'>
  <tr>
    <td style="background-color:#D0E0E3;"><b>Name</b></td>
    <td style="background-color:#D0E0E3;"><b>Job title</b></td>
    <td style="background-color:#D0E0E3;"><b>Contact</b></td>
    <td style="background-color:#D0E0E3;"><b>Address</b></td>
    <td style="background-color:#D0E0E3;"><b>Country</b></td>
  </tr>
<?php
mysql_connect("localhost","root","12345678");
mysql_select_db("form");
mysql_query("set names utf8");
$data=mysql_query("SELECT * FROM form");
for($i=1;$i<=mysql_num_rows($data);$i++){
$result=mysql_fetch_row($data);
?>
  <tr>
    <td><?php echo $result[0]?></td>
    <td><?php echo $result[1]?></td>
    <td><?php echo $result[2]?></td>
    <td><?php echo $result[3]?></td>
    <td><?php echo $result[4]?></td>
  </tr>
<?php
}
?>
</table>
</body>
</html>
