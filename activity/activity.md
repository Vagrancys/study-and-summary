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
   - 列如:
    
   			setContentView(R.layout.activity_main)；
            setContentView(mTextView)；
            setContentView(mTextView,mPramas)；

 - addContentView() --添加视图到现有的活动中
   - 列如: 
    
            addContentView(mTextView，mPramas); 

 - getIntent() --返回开始这个活动的意图
   - 列如: 
    
            Intent intent=getIntent(); 
 - getWindowManager() --返回显示自定义窗口的窗口管理器
   - 列如: 
   
   			WindowManager wm=getWindowManager();
 - getWindow() --返回当前不为null或者不为hide的窗口
   - 列如: 
            
            Window window=getWindow();
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
 - getFragmentManager() --返回相关的交互fragmentmanager碎片
   - 列如: 
   
		    FragmentManager fm=getFragmentManager();

 - findViewById() --如果找到则返回视图否则返回null
   - 列如: 
   
		    TextView text=(TextView) findViewById(R.id.text);

 - getActionBar() --返回该activity的actionBar
   - 列如: 
   
		    ActionBar actionBar=getActionBar();

  - startActivityForResult() --发送一个会返回信息的意图
   - 列如: 
   
		    startActivityForResult(mIntent,ACCOUNT_CODE);
 
  - setResult() --设置返回码
   - 列如: 
   
		    setResult(mResultCode);
  - overridePendingTransition(int enterAnim,int exitAnim) --设置活动的进入和退出动画
   - 列如: 
   
		    overridePendingTransition*(R.anim.enter_anim，R.anim.exit_anim);
   - finish() --结束活动
   - 列如: 
   
		    finish();
   
中级 :

 - getApplication() --返回拥有这个活动的应用程序
   - 列如: 
     
            Application app=getApplication()；
 
 - onConfigurationChanged() --配置发生改变时调用
   - 列如:
    
            public void onConfigurationChanged(Configuration newConfig){}; 
 
 - setActionBar() --设置一个工具条到活动窗口
   - 列如:
    
            setActionBar(mToolbar);

 - onKeyDown() --返回键处理函数,处理点击事件
   - 列如:
    
            @Overrible
            public boolean onKeyDown(int keyCode,KeyEvent event){
                return true;
            }

 - onKeyLongPress() --返回键长压处理函数,处理长压点击事件
   - 列如:
    
            @Overrible
            public boolean onKeyLongPress(int keyCode,KeyEvent event){
                return flase;
            }

 - onKeyUp() --返回键松开处理函数,处理松开事件
   - 列如:
    
            @Overrible
            public boolean onKeyUp(int keyCode,KeyEvent event){
                return flase;
            }

 - onBackPressed() --返回键松开处理函数,处理松开事件
   - 列如:
    
            @Overrible
            public void onBackPressed(){
                super.onBackPressed();
            }

 - onTouchEvent() --触摸事件处理
   - 列如:
    
            @Overrible
            public boolean onTouchEvent(MotionEvent event){
                return super.onTouchEvent(event);
            }

 - ondispathKeyEvent() --是否拦截键事件
   - 列如:
    
            @Override
            public boolean dispatchKeyEvent(KeyEvent event) {
                 return super.dispatchKeyEvent(event);
            }

 - ondispathTouchEvent() --是否拦截触摸事件
   - 列如:
    
            @Override
            public boolean dispatchTouchEvent(MotionEvent ev) {
                 return super.dispatchTouchEvent(ev);
            }


 - onCreateOptionMenu() --创建菜单
   - 列如:
    
            @Override
            public boolean onCreateOptionsMenu(Menu menu) {
          
                 getMenuInflater().inflate(R.menu.menu_browser,menu);
                 return true;
            }

 - onOptionItemSelected() --菜单点击事件
   - 列如:
    
            @Override
            public boolean onOptionsItemSelected(MenuItem item) {
                  switch (item.getItemId()){
                        case android.R.id.home:
                             onBackPressed();
                             break;
                  }
                  return super.onOptionsItemSelected(item);
            }

 - getSystemService(String name) --得到系统服务
   - 列如:
   
            getSystemService(mName);









