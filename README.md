<blockquote>
<h2 id="toc_0">书写规范</h2>
</blockquote>

<h4 id="toc_1">1. 编码方式统一用UTF-8. Android Studio默认已是UTF-8，只要不去改动它就可以了。</h4>

<p><img src="/android/_image/20150709/encodings.png" alt=""></p>

<h4 id="toc_2">2. 缩进统一为4个空格，将Tab size设置为4则可以保证tab键按4个空格缩进。另外，不要勾选上Use tab character，可以保证切换到不同tab长度的环境时还能继续保持统一的4个空格的缩进样式。</h4>

<p><img src="/android/_image/20150709/tab_size.png" alt=""></p>

<h4 id="toc_3">3. 花括号不要单独一行，和它前面的代码同一行。而且，花括号与前面的代码之间用一个空格隔开。</h4>
<div class="codehilite"><pre><span class="kd">public</span> <span class="kt">void</span> <span class="nf">method</span><span class="o">()</span> <span class="o">{</span> <span class="c1">// Good </span>

<span class="o">}</span> 

<span class="kd">public</span> <span class="kt">void</span> <span class="nf">method</span><span class="o">()</span>
<span class="o">{</span> <span class="c1">// Bad</span>
<span class="o">}</span>  

<span class="kd">public</span> <span class="kt">void</span> <span class="nf">method</span><span class="o">(){</span> <span class="c1">// Bad</span>

<span class="o">}</span> 
</pre></div>

<h4 id="toc_4">4. 空格的使用</h4>

<p>if、else、for、switch、while等逻辑关键字与后面的语句留一个空格隔开。</p>
<div class="codehilite"><pre><span class="c1">// Good</span>
<span class="k">if</span> <span class="o">(</span><span class="n">booleanVariable</span><span class="o">)</span> <span class="o">{</span>
    <span class="c1">// TODO while booleanVariable is true</span>
<span class="o">}</span> <span class="k">else</span> <span class="o">{</span>
    <span class="c1">// TODO else</span>
<span class="o">}</span>

<span class="c1">// Bad</span>
<span class="k">if</span><span class="o">(</span><span class="n">booleanVariable</span><span class="o">)</span> <span class="o">{</span>
    <span class="c1">// TODO while booleanVariable is true</span>
<span class="o">}</span><span class="k">else</span> <span class="o">{</span>
    <span class="c1">// TODO else</span>
<span class="o">}</span>
</pre></div>

<p>运算符两边各用一个空格隔开。</p>
<div class="codehilite"><pre><span class="kt">int</span> <span class="n">result</span> <span class="o">=</span> <span class="n">a</span> <span class="o">+</span> <span class="n">b</span><span class="o">;</span> <span class="c1">//Good, = 和 + 两边各用一个空格隔开</span>
<span class="kt">int</span> <span class="n">result</span><span class="o">=</span><span class="n">a</span><span class="o">+</span><span class="n">b</span><span class="o">;</span> <span class="c1">//Bad,=和+两边没用空格隔开</span>
</pre></div>

<p>方法的每个参数之间用一个空格隔开。</p>
<div class="codehilite"><pre><span class="kd">public</span> <span class="kt">void</span> <span class="nf">method</span><span class="o">(</span><span class="n">String</span> <span class="n">param1</span><span class="o">,</span> <span class="n">String</span> <span class="n">param2</span><span class="o">);</span> <span class="c1">// Good，param1后面的逗号与String之间隔了一个空格</span>
<span class="n">method</span><span class="o">(</span><span class="n">param1</span><span class="o">,</span> <span class="n">param2</span><span class="o">);</span> <span class="c1">// Good，方法调用时，param1后面的逗号与param2之间隔了一个空格</span>
<span class="n">method</span><span class="o">(</span><span class="n">param1</span><span class="o">,</span><span class="n">param2</span><span class="o">);</span> <span class="c1">// Bad，没有用一个空格隔开</span>
</pre></div>

<h4 id="toc_5">5. 空行的使用</h4>

<p>将逻辑相关的代码段用空行隔开，以提高可读性。空行也只空一行，不要空多行。在以下情况需用一个空行：</p>

<ul>
<li>两个方法之间</li>
<li>方法内的两个逻辑段之间</li>
<li>方法内的局部变量和方法的第一条逻辑语句之间</li>
<li>常量和变量之间</li>
</ul>

<h4 id="toc_6">6. 当一个表达式无法容纳在一行内时，可换行显示，另起的新行用8个空格缩进。</h4>
<div class="codehilite"><pre><span class="n">someMethod</span><span class="o">(</span><span class="n">longExpression1</span><span class="o">,</span> <span class="n">longExpression2</span><span class="o">,</span> <span class="n">longExpression3</span><span class="o">,</span>  
        <span class="n">longExpression4</span><span class="o">,</span> <span class="n">longExpression5</span><span class="o">);</span>
</pre></div>

<h4 id="toc_7">7. 一行声明一个变量，不要一行声明多个变量，这样有利于写注释。</h4>
<div class="codehilite"><pre><span class="kd">private</span> <span class="n">String</span> <span class="n">param1</span><span class="o">;</span> <span class="c1">// 参数1</span>
<span class="kd">private</span> <span class="n">String</span> <span class="n">param2</span><span class="o">;</span> <span class="c1">// 参数2</span>
</pre></div>

<h4 id="toc_8">8. 行宽设置为100，设置格式化时自动断行到行宽位置。</h4>

<p><img src="/android/_image/20150709/right_margin.jpeg" alt=""></p>

<p><img src="/android/_image/20150709/line_breaks.jpeg" alt=""></p>

<h4 id="toc_9">9. 使用快捷键进行代码自动格式化。</h4>

<p>Windows：CTRL+ALT+L<br />Mac：OPTION+COMMAND+L</p>

<h4 id="toc_10">10. 一个方法最多不要超过40行代码。</h4>

<h4 id="toc_11">11. 范围型的常量用枚举类定义，而不要直接用整型或字符，这样可以减少范围值的有效性检查。</h4>
<div class="codehilite"><pre><span class="c1">// 用枚举类定义，Good</span>
<span class="kd">public</span> <span class="kd">enum</span> <span class="n">CouponType</span> <span class="o">{</span>
    <span class="c1">// 现金券</span>
    <span class="nd">@SerializedName</span><span class="o">(</span><span class="s">&quot;1&quot;</span><span class="o">)</span>
    <span class="n">CASH</span><span class="o">,</span>

    <span class="c1">// 抵用券</span>
    <span class="nd">@SerializedName</span><span class="o">(</span><span class="s">&quot;2&quot;</span><span class="o">)</span>
    <span class="n">DEBIT</span><span class="o">,</span>

    <span class="c1">// 折扣券</span>
    <span class="nd">@SerializedName</span><span class="o">(</span><span class="s">&quot;3&quot;</span><span class="o">)</span>
    <span class="n">DISCOUNT</span>
<span class="o">}</span>

<span class="c1">// 用整型定义，Bad</span>
<span class="kd">public</span> <span class="kd">static</span> <span class="kd">final</span> <span class="kt">int</span> <span class="n">TYPE_CASH</span> <span class="o">=</span> <span class="mi">1</span><span class="o">;</span> <span class="c1">// 现金券</span>
<span class="kd">public</span> <span class="kd">static</span> <span class="kd">final</span> <span class="kt">int</span> <span class="n">TYPE_DEBIT</span> <span class="o">=</span> <span class="mi">2</span><span class="o">;</span> <span class="c1">// 抵扣券</span>
<span class="kd">public</span> <span class="kd">static</span> <span class="kd">final</span> <span class="kt">int</span> <span class="n">TYPE_DISCOUNT</span> <span class="o">=</span> <span class="mi">3</span><span class="o">;</span> <span class="c1">// 折扣券</span>
</pre></div>

<h4 id="toc_12">12. 文字大小的单位统一用sp，元素大小的单位统一用dp。</h4>

<h4 id="toc_13">13. 应用中的字符串统一在strings.xml中定义，然后在代码和布局文件中引用。</h4>

<h4 id="toc_14">14. 颜色值统一在colors.xml中定义，然后在代码和布局文件中引用。另外，不要在代码和布局文件中引用系统的颜色，除了透明。</h4>

<blockquote>
<h2 id="toc_15">命名规范</h2>
</blockquote>

<h4 id="toc_16">1. 包命名</h4>

<p>域名反写+项目名称+模块名称，全部单词用小写字母。<br />例如，我的KAndroid项目的Model模块包名如下：</p>
<div class="codehilite"><pre><span class="n">me</span><span class="o">.</span><span class="na">keeganlee</span><span class="o">.</span><span class="na">kandroid</span><span class="o">.</span><span class="na">model</span>
</pre></div>

<h4 id="toc_17">2. 类和接口命名</h4>

<p>使用大驼峰规则，用名词或名词词组命名，每个单词的首字母大写。<br />以下为几种常用类的命名：</p>

<ul>
<li>activity类，命名以Activity为后缀，如：LoginActivity</li>
<li>fragment类，命名以Fragment为后缀，如：ShareDialogFragment</li>
<li>service类，命名以Service为后缀，如：DownloadService</li>
<li>adapter类，命名以Adapter为后缀，如：CouponListAdapter</li>
<li>工具类，命名以Util为后缀，如：EncryptUtil</li>
<li>模型类，命名以BO为后缀，如：CouponBO</li>
<li>接口实现类，命名以Impl为后缀，如：ApiImpl</li>
</ul>

<h4 id="toc_18">3. 方法命名</h4>

<p>使用小驼峰规则，用动词命名，第一个单词的首字母小写，其他单词的首字母大写。<br />以下为几种常用方法的命名：</p>

<ul>
<li>初始化方法，命名以init开头，例：initView</li>
<li>按钮点击方法，命名以to开头，例：toLogin</li>
<li>设置方法，命名以set开头，例：setData</li>
<li>具有返回值的获取方法，命名以get开头，例：getData</li>
<li>通过异步加载数据的方法，命名以load开头，例：loadData</li>
<li>布尔型的判断方法，命名以is或has，或具有逻辑意义的单词如equals，例：isEmpty</li>
</ul>

<h4 id="toc_19">4. 控件缩写</h4>

<table><thead>
<tr>
<th>控件</th>
<th>缩写</th>
<th>控件</th>
<th>缩写</th>
</tr>
</thead><tbody>
<tr>
<td>TextView</td>
<td>txt</td>
<td>EditText</td>
<td>edt</td>
</tr>
<tr>
<td>Button</td>
<td>btn</td>
<td>ImageButton</td>
<td>ibtn</td>
</tr>
<tr>
<td>ImageView</td>
<td>img</td>
<td>ListView</td>
<td>list</td>
</tr>
<tr>
<td>RadioGroup</td>
<td>group</td>
<td>RadioButton</td>
<td>rbtn</td>
</tr>
<tr>
<td>ProgressBar</td>
<td>progress</td>
<td>SeekBar</td>
<td>seek</td>
</tr>
<tr>
<td>CheckBox</td>
<td>chk</td>
<td>Spinner</td>
<td>spinner</td>
</tr>
<tr>
<td>TableLayout</td>
<td>table</td>
<td>TableRow</td>
<td>row</td>
</tr>
<tr>
<td>LinearLayout</td>
<td>llayout</td>
<td>RelativeLayout</td>
<td>rlayout</td>
</tr>
<tr>
<td>ScrollView</td>
<td>scroll</td>
<td>SearchView</td>
<td>search</td>
</tr>
<tr>
<td>TabHost</td>
<td>host</td>
<td>TabWidget</td>
<td>widget</td>
</tr>
</tbody></table>

<h4 id="toc_20">5. 常量命名</h4>

<p>全部为大写单词，单词之间用下划线分开。</p>
<div class="codehilite"><pre><span class="kd">public</span> <span class="kd">final</span> <span class="kd">static</span> <span class="kt">int</span> <span class="n">PAGE_SIZE</span> <span class="o">=</span> <span class="mi">20</span><span class="o">;</span>
</pre></div>

<h4 id="toc_21">6. 变量命名</h4>

<p>{范围描述+}意义描述+类型描述的组合，用驼峰式，首字母小写。</p>
<div class="codehilite"><pre><span class="kd">private</span> <span class="n">TextView</span> <span class="n">headerTitleTxt</span><span class="o">;</span> <span class="c1">// 标题栏的标题</span>
<span class="kd">private</span> <span class="n">Button</span> <span class="n">loginBtn</span><span class="o">;</span> <span class="c1">// 登录按钮</span>
<span class="kd">private</span> <span class="n">CouponBO</span> <span class="n">couponBO</span><span class="o">;</span> <span class="c1">// 券实例</span>
</pre></div>

<h4 id="toc_22">7. 控件id命名</h4>

<p>控件缩写_{范围_}意义，范围可选，只在有明确定义的范围内才需要加上。</p>
<div class="codehilite"><pre><span class="o">&lt;!--</span> <span class="n">这是标题栏的标题</span> <span class="o">--&gt;</span>
<span class="o">&lt;</span><span class="n">TextView</span>
    <span class="nl">android:</span><span class="n">id</span><span class="o">=</span><span class="s">&quot;@+id/txt_header_title&quot;</span>
    <span class="o">...</span> <span class="o">/&gt;</span>

<span class="o">&lt;!--</span> <span class="n">这是登录按钮</span> <span class="o">--&gt;</span>
<span class="o">&lt;</span><span class="n">Button</span>
    <span class="nl">android:</span><span class="n">id</span><span class="o">=</span><span class="s">&quot;@+id/btn_login&quot;</span>
    <span class="o">...</span> <span class="o">/&gt;</span>
</pre></div>

<h4 id="toc_23">8. layout命名</h4>

<p>组件类型_{范围_}功能，范围可选，只在有明确定义的范围内才需要加上。<br />以下为几种常用的组件类型命名：</p>

<ul>
<li>activity_{范围_}功能，为Activity的命名格式</li>
<li>fragment_{范围_}功能，为Fragment的命名格式</li>
<li>dialog_{范围_}功能，为Dialog的命名格式</li>
<li>item_list_{范围_}功能，为ListView的item命名格式</li>
<li>item_grid_{范围_}功能，为GridView的item命名格式</li>
<li>header_list_{范围_}功能，为ListView的HeaderView命名格式</li>
<li>footer_list_{范围_}功能，为ListView的FooterView命名格式</li>
</ul>

<h4 id="toc_24">9. strings的命名</h4>

<p>类型_{范围_}功能，范围可选。<br />以下为几种常用的命名：</p>

<ul>
<li>页面标题，命名格式为：title_页面</li>
<li>按钮文字，命名格式为：btn_按钮事件</li>
<li>标签文字，命名格式为：label_标签文字</li>
<li>选项卡文字，命名格式为：tab_选项卡文字</li>
<li>消息框文字，命名格式为：toast_消息</li>
<li>编辑框的提示文字，命名格式为：hint_提示信息</li>
<li>图片的描述文字，命名格式为：desc_图片文字</li>
<li>对话框的文字，命名格式为：dialog_文字</li>
<li>menu的item文字，命名格式为：action_文字</li>
</ul>

<h4 id="toc_25">10. colors的命名</h4>

<p>前缀{_控件}{_范围}{_后缀}，控件、范围、后缀可选，但控件和范围至少要有一个。</p>

<ul>
<li>背景颜色，添加bg前缀</li>
<li>文本颜色，添加text前缀</li>
<li>分割线颜色，添加div前缀</li>
<li>区分状态时，默认状态的颜色，添加normal后缀</li>
<li>区分状态时，按下时的颜色，添加pressed后缀</li>
<li>区分状态时，选中时的颜色，添加selected后缀</li>
<li>区分状态时，不可用时的颜色，添加disable后缀</li>
</ul>

<h4 id="toc_26">11. drawable的命名</h4>

<p>前缀{_控件}{_范围}{_后缀}，控件、范围、后缀可选，但控件和范围至少要有一个。</p>

<ul>
<li>图标类，添加ic前缀</li>
<li>背景类，添加bg前缀</li>
<li>分隔类，添加div前缀</li>
<li>默认类，添加def前缀</li>
<li>区分状态时，默认状态，添加normal后缀</li>
<li>区分状态时，按下时的状态，添加pressed后缀</li>
<li>区分状态时，选中时的状态，添加selected后缀</li>
<li>区分状态时，不可用时的状态，添加disable后缀</li>
<li>多种状态的，添加selector后缀（一般为ListView的selector或按钮的selector）</li>
</ul>

<h4 id="toc_27">12. 动画文件命名</h4>

<p>动画类型_动画方向。</p>

<ul>
<li>fade_in，淡入</li>
<li>fade_out，淡出</li>
<li>push_down_in，从下方推入</li>
<li>push_down_out，从下方推出</li>
<li>slide_in_from_top，从头部滑动进入</li>
<li>zoom_enter，变形进入</li>
<li>shrink_to_middle，中间缩小</li>
</ul>

<blockquote>
<h2 id="toc_28">注释规范</h2>
</blockquote>

<h4 id="toc_29">1. 文件头注释</h4>

<p>文件顶部统一添加版权声明，声明的格式如下：</p>
<div class="codehilite"><pre><span class="cm">/**</span>
<span class="cm"> * Copyright (c) 2015. Keegan小钢 Inc. All rights reserved.</span>
<span class="cm"> */</span>
</pre></div>

<h4 id="toc_30">2. 类和接口注释</h4>

<p>类和接口统一添加javadoc注释，格式如下：</p>
<div class="codehilite"><pre><span class="cm">/**</span>
<span class="cm"> * 类或接口的描述信息</span>
<span class="cm"> *</span>
<span class="cm"> * @author ${USER}</span>
<span class="cm"> * @date ${DATE}</span>
<span class="cm"> */</span>
</pre></div>

<h4 id="toc_31">3. 方法注释</h4>

<p>下面几种方法，都必须添加javadoc注释，说明该方法的用途和参数说明，以及返回值的说明。</p>

<ul>
<li>接口中定义的所有方法</li>
<li>抽象类中自定义的抽象方法</li>
<li>抽象父类的自定义公用方法</li>
<li>工具类的公用方法</li>
</ul>
<div class="codehilite"><pre><span class="cm">/**</span>
<span class="cm"> * 登录</span>
<span class="cm"> *</span>
<span class="cm"> * @param loginName 登录名</span>
<span class="cm"> * @param password  密码</span>
<span class="cm"> * @param listener  回调监听器</span>
<span class="cm"> */</span>
<span class="kd">public</span> <span class="kt">void</span> <span class="nf">login</span><span class="o">(</span><span class="n">String</span> <span class="n">loginName</span><span class="o">,</span> <span class="n">String</span> <span class="n">password</span><span class="o">,</span> <span class="n">ActionCallbackListener</span><span class="o">&lt;</span><span class="n">Void</span><span class="o">&gt;</span> <span class="n">listener</span><span class="o">);</span>
</pre></div>

<h4 id="toc_32">4. 变量和常量注释</h4>

<p>下面几种情况下的常量和变量，都要添加注释说明，优先采用右侧//来注释，若注释说明太长则在上方添加注释。</p>

<ul>
<li>接口中定义的所有常量</li>
<li>公有类的公有常量</li>
<li>枚举类定义的所有枚举常量</li>
<li>实体类的所有属性变量</li>
</ul>
<div class="codehilite"><pre><span class="kd">public</span> <span class="kd">static</span> <span class="kd">final</span> <span class="kt">int</span> <span class="n">TYPE_CASH</span> <span class="o">=</span> <span class="mi">1</span><span class="o">;</span> <span class="c1">// 现金券</span>
<span class="kd">public</span> <span class="kd">static</span> <span class="kd">final</span> <span class="kt">int</span> <span class="n">TYPE_DEBIT</span> <span class="o">=</span> <span class="mi">2</span><span class="o">;</span> <span class="c1">// 抵扣券</span>
<span class="kd">public</span> <span class="kd">static</span> <span class="kd">final</span> <span class="kt">int</span> <span class="n">TYPE_DISCOUNT</span> <span class="o">=</span> <span class="mi">3</span><span class="o">;</span> <span class="c1">// 折扣券</span>

<span class="kd">private</span> <span class="kt">int</span> <span class="n">id</span><span class="o">;</span>                <span class="c1">// 券id</span>
<span class="kd">private</span> <span class="n">String</span> <span class="n">name</span><span class="o">;</span>           <span class="c1">// 券名称</span>
<span class="kd">private</span> <span class="n">String</span> <span class="n">introduce</span><span class="o">;</span>      <span class="c1">// 券简介</span>
</pre></div>

<hr>
