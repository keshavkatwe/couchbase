<h2>Configuration of Couchbase php sdk 2.0.3</h2>

Step 1: First make sure you have install <b>xampp with php 5.5</b> version in windows.Because 5.6 is not supported by couchbase.

Step 2: Copy <b>php_couchbase.dll</b> to <b>C:\xampp\php\ext</b>. And copy file <b>libcouchbase.dll</b> to <b>C:\xampp\php</b> and <b>C:\xampp\apache\bin</b>.

Step 3: Add <b>extension=php_couchbase.dll</b> line to php.ini

Step 4: Restart Xampp. And it is good to go.

Example Code:
<pre>
//connection to cluster
$clusterConnection = new CouchbaseCluster('couchbase://localhost');
//connection to bucket
$bucket = $clusterConnection->openBucket('default');
//array of data to be inserted into document
$data = array(
	'Name' => 'Keshav Katwe',
	'College' => 'KLE'
);
//insert into document
$result = $bucket->insert('101', $data);
var_dump($result);
</pre>
