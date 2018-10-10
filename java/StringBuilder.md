## StringBuilder高性能优化
> 局限性,优化后,同时拼接多个String时,需手动创建额外的StringBuilder,增加编码复杂度;

Q:Java编译优化后＋和StringBuilder的效果一样
A:  单条语句中的+会被编译为StringBuilder的方式拼接,但多条语句(如for循环中拼接)会重复创建StringBuilder,
	因此最好直接写成StringBuilder形式;
	
Q: StringBuilder不是线程安全的，为了“安全”起见最好还是用StringBuffer；
A: 大部分情况不涉及到跨进程的字符串拼接;同时在复用StringBuilder对象时,使用ThreadLocal修饰,为每个线程单独
	创建StringBuilder,避免线程安全问题;
	
* 常见的StringBuilder性能问题
1. 使用默认创建,StringBuilder中的char[]长度为16,当拼接内容过多时,会触发多次数组的扩容操作
2. StringBuilder.toString()方法,String会复制整个char[]再操作,保证数据的安全性;

* 因此,可以采取复用StringBuilder的方式提升性能
	* 复用的StringBuiler 随着使用次数的增长,扩容的情况会递减,也不必思考如何设置合适的长度;
	* 减少StringBuilder的创建操作;
	* 使用StringBuilder.setLength(0)进行内容的重置,该操作仅重置count指针,toString是仅使用0-count位置的
	的char,不必担心数据被旧内容污染;
	
	