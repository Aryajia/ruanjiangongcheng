## 为什么要进行单元测试
1.单元测试不但会使你的工作完成得更轻松。而且会令我们的设计会变得更好，甚至大大减少你花在调试上面的时间 2.提高代码质量 3.


减少bug，快速定位bug。
可以验证单元代码和详细设计文档的一致性，跟踪详细设计文档中设计的实现，发现详细设计文档中存在的错误;发现在编码过程中引入的错误编码过程中引入的错误包含两类:和设计不符引入的错误;和设计相符但由于编码出现疏漏导致错误。
## java,冒泡排序
**冒泡代码
```
	public class MaoPao {
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int[]a= {1,32,12,3,5,66,42,0};
		for(int i=0;i<a.length-1;i++) {
			for(int j=0;j<a.length-1-i;j++) {
				if(a[j]<a[j+1]) {
					int t=a[j];
					a[j]=a[j+1];
					a[j+1]=t;
		}
        }
    }
		for(int i=0;i<a.length ;i++) {
	System.out.print(a[i]+" ");}  
```
**单元测试的代码**
```
一：import org.junit.Test：
 public class t {
 
	//语句覆盖
	@Test
	public void test1() {
		int[] arr= {4,3,2,1};
		test t=new test();
		t.BubbleSort(arr);
	}
	
	//判定覆盖
	@Test
	public void test2() {
		int[] arr= {1,2,3,4};
		test t=new test();
		t.BubbleSort(arr);
	}
	@Test
	public void test3() {
		int[] arr= {4,3,2,1};
		test t=new test();
		t.BubbleSort(arr);
	}
	
	//条件覆盖
	@Test
	public void test4() {
		int[] arr= {1,2,3,4};
		test t=new test();
		t.BubbleSort(arr);
	}
	@Test
	public void test5() {
		int[] arr= {4,3,2,1};
		test t=new test();
		t.BubbleSort(arr);
	}
	
	//路径覆盖
	@Test
	public void test6() {
		int[] arr= {1,2,3,4};
		test t=new test();
		t.BubbleSort(arr);
	}
	@Test
	public void test7() {
		int[] arr= {4,3,2,1};
		test t=new test();
		t.BubbleSort(arr);
	}
	
}
```  
 **测试用例**  
  用例编号|输入|输出|用例说明
  -------|----|----|-------
   --1-- |arr={4,3,2,1}|1,2,3,4|语句覆盖
   --2-- |arr={1,2,3,4}|1,2,3,4|判定覆盖
   --3-- |arr={4,3,2,1}|1,2,3,4|判定覆盖
   --4-- |arr={1,2,3,4}|1,2,3,4|条件覆盖
   --5-- |arr={4,3,2,1}|1,2,3,4|条件覆盖
   --6-- |arr={1,2,3,4}|1,2,3,4|路径覆盖
   --7-- |arr={4,3,2,1}|1,2,3,4|路径覆盖
   

