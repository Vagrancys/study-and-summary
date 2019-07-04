## activity ##

### 简单说明:可以包含用户界面的组件，用于和用户进行交互。 ###

	public class MainActivity extends Activity{
		@Override
		protected void onCreate(Bundle savedInstanceState){
			super.onCreate(saveInstanceState)；
		}
	}

初级 :
	
 - setContentView()  --设置布局文件 
   - 列如:setContentView(R.layout.activity_main)；
 - getIntent() --返回开始这个活动的意图
   - 列如: Intent intent=getIntent(); 
 - getWindowManager() --返回显示自定义窗口的窗口管理器
     - 列如: 无;
 - getWindow() --返回当前不为null或者不为hide的窗口
   - 列如: 无;
 - onCreate() --活动开始时调用，最初始化
   - 列如: (活动被重新初始化或者关闭，savedInstanceState可以恢复大部分数据)
    
		    protected void onCreate(Bundle savedInstanceState){
		         	super.onCreate(savedInstanceState);
					-----
		    } 

 - onStart() --执行onCreate完之后调用或者执行onRestart之后调用，活动由不可见变为可见时
   - 列如: 
   
		    protected void onStart(){
		         	super.onStart();
					-----
		    } 

 - onRestart() --用户回到该活动时调用本函数，活动重新开始显示
   - 列如: 
   
		    protected void onRestart(){
		         	super.onRestart();
					-----
		    } 

 - onResume() --活动开始与用户交互，可以做些简单的交互
   - 列如: 
   
		    protected void onResume(){
		         	super.onResume();
					-----
		    } 

 - onPause() --系统准备启动或者恢复另一个活动时调用，可以在该函数做些如停止动画或其他解放资源
   - 列如: 
   
		    protected void onPause(){
		         	super.onPause();
					-----
		    } 

 - onStop() --活动完全不可见时调用
   - 列如: 
   
		    protected void onStop(){
		         	super.onStop();
					-----
		    } 

 - onDestroy() --活动要被销毁之前调用
   - 列如: 
   
		    protected void onDestroy(){
		         	super.onDestroy();
					-----
		    }
中级 :

 - getApplication() --返回拥有这个活动的应用程序
   - 列如: 无；
 - 