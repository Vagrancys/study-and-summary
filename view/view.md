## view ##

### 简单说明:负责视图的绘制,响应和显示。 ###

初级 :

   - setOnScrollChangeListener(OnScrollChangeListener l)  --设置视图滑动变化监听器 
      - 列如:
      - 
               setOnScrollChangeListener(mListener);
   			

   - setOnFocusChangeListener(OnFocusChangeListener l)  --设置视图焦点变化监听器 
      - 列如:
      - 
               setOnFocusChangeListener(mListener);
   			
   - setOnClickListener(OnClickListener l)  --设置视图点击监听器 
      - 列如:
      - 
               setOnClickListener(mListener);
   			
   - setOnLongClickListener(OnLongClickListener l)  --设置视图长点击监听器 
      - 列如:
      - 
               setOnLongClickListener(mListener);
   	
   - setOnKeyListener(OnKeyListener l)  --设置视图键盘监听器 
      - 列如:
      - 
               setOnKeyListener(mListener);
   	
   - setOnTouchListener(OnTouchListener l)  --设置视图触摸监听器 
      - 列如:
      - 
               setOnTouchListener(mListener);

   - setVisibility(int visibility)  --设置视图显示状态 
      - 列如:
      - 
               setVisibility(View.VISIBLE);
   - setEnabled(boolean enabled)  --设置视图可用状态
      - 列如:
      - 
               setEnabled(true);
   
  - onTouchEvent(MotionEvent event)  --设置视图触摸事件处理
      - 列如:
      - 
               @Override
               public void onTouchEvent(MotionEvent event){
                    super.onTouchEvent(event);
               }
  - onScrollChanged(int 路，int t，int oldl, int oldt)  --设置视图滑动事件处理
      - 列如:
      - 
               @Override
               public void onScrollChanged(int l，int t，int oldl，int oldt){
                    super.onScrollChanged(l，t，oldl，oldt);
               }   	

   - setScrollX(int value)  --设置视图沿x轴移动
      - 列如:
      - 
               setScrollX(100);

   - setScrollY(int value)  --设置视图沿y轴移动
      - 列如:
      - 
               setScrolly(100);
      