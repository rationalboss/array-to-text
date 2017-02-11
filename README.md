ArrayToText
---

ArrayToText will transform a PHP array to a textual table. Original script: http://tonylandis.com/php/php-text-tables-class/.

```
<?php

$data = array(
	array('company'=>'AIG', 'id'=>1, 'balance'=> '-$99,999,999,999.00'),
	array('company'=>'Wachovia', 'id'=>2, 'balance'=> '-$10,000,000.00'),
	array('company'=>'HP', 'id'=>3, 'balance'=> '$555,000.000.00'),
	array('company'=>'IBM', 'id'=>4, 'balance'=> '$12,000.00')
);

$renderer = new ArrayToText($data);
$renderer->showHeaders(true);
$renderer->render();


// Using Composer:

/*

"require": {
	"rationalboss/array-to-text": "dev-master"
}

*/

$data = array(
	array('company'=>'AIG', 'id'=>1, 'balance'=> '-$99,999,999,999.00'),
	array('company'=>'Wachovia', 'id'=>2, 'balance'=> '-$10,000,000.00'),
	array('company'=>'HP', 'id'=>3, 'balance'=> '$555,000.000.00'),
	array('company'=>'IBM', 'id'=>4, 'balance'=> '$12,000.00')
);
$renderer = new \rationalboss\util\ArrayToText($data);
$renderer->showHeaders(true);
$renderer->render();

?>
```

Sample Output:

```
+----------+----+---------------------+
| COMPANY  | ID |       BALANCE       |
+----------+----+---------------------+
| AIG      | 1  | -$99,999,999,999.00 |
| Wachovia | 2  | -$10,000,000.00     |
| HP       | 3  | $555,000.000.00     |
| IBM      | 4  | $12,000.00          |
+----------+----+---------------------+
```