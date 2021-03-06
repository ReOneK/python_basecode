经典的八皇后问题
	==python 基础编程内的一个解释递归迭代器的一个案例
	
	皇后可以在横、竖、斜线上不限步数地吃掉其他棋子。如何将8个皇后放在棋盘上（有8 * 8个方格），
使它们谁也不能被吃掉！这就是著名的八皇后问题。

	对于某个满足要求的8皇后的摆放方法，定义一个元组a与之对应，
即a=（0，2，3，2，5，6，8，5），其中a[0]=0,表示第一行第一个位置

详细解释：
	第一行放置一个皇后，第二行放置一个皇后， 第N行也放置一个皇后… 这样， 
	可以保证每行都有一个皇后，那么各行的皇后应该放置在那一列呢，
	算法通过循环来完成，在循环的过程中， 一旦找到一个合适的列，
	则该行的皇后位置确定，则继续进行下一行的皇后的位置的确定。由于每一行确定
	皇后位置的方式相似，所以可以使用递归法。一旦最后 一行的皇后位置确定，则可以得到一组解。
	找到一组解之后， 之前确定皇后应该放置在哪一列的循环其实才进行了一轮循环的， 
	算法通过该循环遍历所有的列，以此确定每一行所有可能的列的位置。在从一轮循环进入下一轮循环之前，
	算法需要清除在上一轮被标记为不可放置皇后的标记，也就是回溯。因为进入下一轮循环之后，
	同一行的皇后的列的位置会发生了变化，之前被标记为不可放置皇后的列和正反对角线位置都已经失效。

ps:还涉及到算法中的回溯问题，就是用递归替代了无数的for循环