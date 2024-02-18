## 第3章 目标文件里面有什么

### 3.1目标文件的格式

* 可执行文件的格式主要是 Windows 下的 `PE` 和 Linux 的 `ELF` ，它们都是 `COFF`格式的变种
*  目标文件就是源代码编译后但未进行链接的那些中间文件
*  动态链接库(Windows的 `.dll` 和 Linux 的 `.so`)及静态链接库(Windows的 `.lib` 和 Linux 的 `.a`) 都是按照可执行文件存粗的
*  在 Linux 下使用 file 命令来查看相应的文件格式

### 3.3 挖掘 SimpleSection.o

* gcc -c SimpleSection 只编译不连接
* objdump -h SimpleSection.o （-h 基本信息, -x 更多信息)
* readelf, 它是专门针对 elf 文件格式的解析器
* size 可以用来查看 elf 文件的代码段、数据段和 bbs段长度


**3.3.1 代码段**

* -s 所有段的内容以十六进制的方式打印出来
* -d 将所有包含指令的段反汇编


**3.4.1 文件头**

* readelf -h SimpleSection.o