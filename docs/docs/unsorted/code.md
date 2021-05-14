<?

$array = [6, 7, 8, 9, 10, 11, 12];

$filter = array_filter($array, function ($data) {
    return $data & 2;
});

print_r($filter);

                    $tables[] = array_map(function ($item) {
                        return $item;
                    }, $this->modulesTables[$module['Keyword']]);

for ($i = 0, $j = 0; $i < $cnt; $i++, $j++) {

}

======================================

$default = 1000;
for ($i = 0; $i < sizeof($nums); $i++) {
    if ($nums[$i] === $target) {
        $default = min($default, abs($i - $start));
    }
}

======================================

$reverceStrign = "";
for ($i = $length - 1; $i >= 0; $i--) {
    $reverceStrign .= $s[$i];
}

======================================

$index = 0;

for ($i = 0; $i < count($nums); $i++) {
    if ($nums[$i] == $target) {
        return $i;
    } elseif (($target > $nums[$i] && $target < $nums[$i + 1]) || ($target > $nums[count($nums)-1])) {
        $index = $i + 1;
    }
}

return $index;

======================================

1800. Maximum Ascending Subarray Sum

$res = $cur = $nums[0];
for ($i = 1; $i < count($nums); $i++) {
    if ($nums[$i - 1] < $nums[$i]) {
        $cur += $nums[$i];
        $res = max($res, $cur);
    } else {
        $cur = $nums[$i];
    }
}

return $res;

======================================

$left = 0;
$right = sizeof($numbers) - 1;
while ($left < $right) {
    if ($numbers[$left] + $numbers[$right] < $target) {
        $left++;
    } elseif ($numbers[$left] + $numbers[$right] > $target) {
        $right--;
    } elseif ($numbers[$left] + $numbers[$right] == $target) {
        return [$left + 1, $right + 1];
    }
}

======================================

$current[0] = $nums[0];
for($i = 1; $i < sizeof($nums); $i++) {
    $current[$i] = $nums[$i] + $current[$i-1];
}

======================================

or ($i = 0; $i < count($nums); $i++) {
    for ($j = 1 + $i; $j < count($nums); $j++) {
        if ($nums[$i] + $nums[$j] == $target) {
            return [$i, $j];
        }
    }
}