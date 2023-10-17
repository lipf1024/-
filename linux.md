- cpu满载运行的命令
  ```
  for i in `seq 1 $(cat /proc/cpuinfo |grep "physical id" |wc -l)`; do dd if=/dev/zero of=/dev/null & done
  ```
- 根目录日志搜索命令
  ```
  grep -rn 'key1' * |grep 'key2'
  ```
