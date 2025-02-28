# WMZDailog - 功能最多样式最多的弹窗，支持普通/微信底部/提示/加载框/日期/地区/日历/选择/编辑/分享/菜单/吐司/自定义弹窗等,支持多种动画,链式编程调用，所有属性均可定制

 [![Platform](https://img.shields.io/badge/platform-iOS-red.svg)](https://developer.apple.com/iphone/index.action) 
 [![CocoaPods Compatible](https://img.shields.io/cocoapods/v/WMZDialog.svg)](https://img.shields.io/cocoapods/v/WMZDialog.svg)
 [![License](https://img.shields.io/badge/license-MIT-blue.svg)](http://mit-license.org) 
 
特性
==============
- 链式语法 结构优雅
- 支持任意位置视图的弹窗(包括滚动视图)
- 支持单选/多选
- 支持地区1/2/3级联动(自定义地区数据)
- 支持无限级联动
- 支持加载框
- 支持提示框
- 支持横竖屏
- 支持时间选择(年月日时分秒自由组合+最大最小时间限制)
- 支持支持多种动画
- 支持所有字体颜色/字体大小的设置
- 支持支付视图
- 支持ios13Persent弹窗
- 支持日历
- 支持菜单选择
- 支持默认选中
- 支持所有列表cell样式的自定义
- 支持自定义弹窗
- 支持多弹窗优先级
- 支持自定义深色模式

## 调用枚举说明
```
typedef enum : NSUInteger{
    DialogTypeNornal = 1,           //默认弹窗
    DialogTypeSheet,                //底部弹窗
    DialogTypeAuto,                 //默认弹窗自动消失
    DialogTypePay,                  //支付密码框
    DialogTypeShare,                //带分享的弹窗
    DialogTypeWrite,                //带编辑框的弹窗
    DialogTypeSelect,               //带选择的弹窗
    DialogTypePickSelect,           //拾取器弹窗
    DialogTypeTime,                 //带倒计时的弹窗
    DialogTypePop,                  //下拉列表选择弹窗
    DialogTypeDown,                 //带下载的弹窗
    DialogTypeMenusSelect,          //下拉无限级菜单弹窗
    DialogTypeAdvertisement,        //广告弹窗
    DialogTypeLocation,             //地区选择
    DialogTypeDatePicker,           //日期选择
    DialogTypeTabbarMenu,           //闲鱼 微博+号底部弹窗
    DialogTypeNaviMenu,             //QQ顶部弹窗
    DialogTypeLoading,              //加载框
    DialogTypeCardPresent ,         //ios13 present效果
    DialogTypeCalander,             //日历弹窗
    DialogTypeToast,                //吐司
    DialogTypeMyView,               //自定义弹窗
}DialogType;
```

| 弹窗类型                | 图片                       |
|-----------------------|-----------------------------------------------------|
|  默认弹窗              | ![DialogTypeNornal.gif](https://upload-images.jianshu.io/upload_images/9163368-8c8a36d86d973324.gif?imageMogr2/auto-orient/strip)|
|  底部弹窗              | ![DialogTypeSheet.gif](https://upload-images.jianshu.io/upload_images/9163368-bcc819412d5e76c5.gif?imageMogr2/auto-orient/strip) |
|  自动消失hud弹窗              |![DialogTypeAuto.gif](https://upload-images.jianshu.io/upload_images/9163368-a75a65e5db1283cd.gif?imageMogr2/auto-orient/strip)|
|  支付密码框              | ![DialogTypePay.gif](https://upload-images.jianshu.io/upload_images/9163368-767cda14847439c0.gif?imageMogr2/auto-orient/strip)|
|  带分享的弹窗              | ![DialogTypeShare.gif](https://upload-images.jianshu.io/upload_images/9163368-8a68f0b5607126b2.gif?imageMogr2/auto-orient/strip)|
|  带编辑框的弹窗              | ![DialogTypeWrite.gif](https://upload-images.jianshu.io/upload_images/9163368-e3b3601ffa320216.gif?imageMogr2/auto-orient/strip) |
|  带选择的弹窗             | ![DialogTypeSelect.gif](https://upload-images.jianshu.io/upload_images/9163368-c095979faf7da4f9.gif?imageMogr2/auto-orient/strip) |
|  拾取器弹窗             | ![DialogTypePickSelect.gif](https://upload-images.jianshu.io/upload_images/9163368-0532f85530352d04.gif?imageMogr2/auto-orient/strip)|
|  带倒计时的弹窗             | ![DialogTypeTime.gif](https://upload-images.jianshu.io/upload_images/9163368-ee7369998dd6d31a.gif?imageMogr2/auto-orient/strip)|
|  下拉列表选择弹窗            |![DialogTypePop.gif](https://upload-images.jianshu.io/upload_images/9163368-4063027ccdaf179a.gif?imageMogr2/auto-orient/strip)|
|  带下载的弹窗             |![DialogTypeDown.gif](https://upload-images.jianshu.io/upload_images/9163368-73435002a47fba68.gif?imageMogr2/auto-orient/strip)|
|  下拉无限级菜单弹窗          |![DialogTypeMenusSelect.gif](https://upload-images.jianshu.io/upload_images/9163368-ba777c81f258bc95.gif?imageMogr2/auto-orient/strip)|
|  地区弹窗          |![DialogTypeLocation.gif](https://upload-images.jianshu.io/upload_images/9163368-443ae1d45ab85eaa.gif?imageMogr2/auto-orient/strip)|
|  日期选择弹窗          |![DialogTypeDatePicker.gif](https://upload-images.jianshu.io/upload_images/9163368-87e47adc2a96d01e.gif?imageMogr2/auto-orient/strip)|
| 顶部菜单弹窗           |![DialogTypeNaviMenu.gif](https://upload-images.jianshu.io/upload_images/9163368-6f8259333ecd64ad.gif?imageMogr2/auto-orient/strip)|
| 底部菜单弹窗           |![DialogTypeTabbarMenu.gif](https://upload-images.jianshu.io/upload_images/9163368-79d72089a0ffc133.gif?imageMogr2/auto-orient/strip)|
|  加载框          |![DialogTypeLoading.gif](https://upload-images.jianshu.io/upload_images/9163368-2cd96f99245809cb.gif?imageMogr2/auto-orient/strip)|
|  ios13 present效果  |![DialogTypeCardPresent.gif](https://upload-images.jianshu.io/upload_images/9163368-663d6c5ce638ef12.gif?imageMogr2/auto-orient/strip)|
|  日历弹窗       |![DialogTypeCalander.gif](https://upload-images.jianshu.io/upload_images/9163368-39f704f1b01e0acf.gif?imageMogr2/auto-orient/strip)|
|  自定义弹窗       |![DialogTypeMyView.gif](https://upload-images.jianshu.io/upload_images/9163368-5fd959fca5baad8c.gif?imageMogr2/auto-orient/strip)|


## 参数说明(详情使用看demo)
### DialogTypeNornal/DialogTypeSheet/DialogTypeSelect。。。
| 可配置通用参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wData                | id        | 数据源                             |
| wShowAnimation      | DialogShowAnination      | 出现的动画  default AninatonZoomIn |
| wHideAnimation                | DialogHideAnination| 消失的动画   default  none                 |
| wAnimationDurtion                | NSTimeInterval        | 动画时间  default 0.8                          |
| wParentVC      | UIViewController      | 父控制器 default 当前VC                                  |
| wType                | DialogType      | 弹窗类型   default  DialogTypeNornal            |
| wWidth                | CGFloat        | 弹窗视图的宽度  default  500                           |
| wHeight      | CGFloat      | 弹窗视图的高度 default 自适应高度 300                        |
| wMainOffsetY                | CGFloat      | Y间距   default 20              |
| wMainOffsetX                | CGFloat        | X间距 default  15                            |
| wMainBtnHeight                | CGFloat      | 按钮高度   default  60                  |
| wMyCell                | UITableViewCell        | 自定义cell                              |
| wMainToBottom                | BOOL     | 视图在最底部  default NO                |
| wLineColor                | UIColor        |  线条的颜色 default 333333                             |
| wLineAlpha                | CGFLoat      |  线条的透明度 default 0.5              |
| wTitle                | NSString        | 标题文本  default 标题                             |
| wMessage                | NSString        | 内容文本 default 内容                             |
| wOKTitle                | NSString      | 确定按钮的文本 default 确定                |
| wCancelTitle                | NSString        | 取消按钮的文本   default 取消                           |
| wOKColor                | UIColor        |  确定按钮的颜色     default 0xFF9900                          |
| wCancelColor                | UIColor | 取消按钮的颜色 default 0x666666                             |
| wMainBackColor                | UIColor | 弹出视图的背景颜色     default 0xffffff            |
| wTitleColor                | UIColor        | 标题文本的颜色   default 0x333333                            |
| wMessageColor                | UIColor        | 内容文本的颜色   default 0x333333                            |
| wOKFont                | CGFLoat        | 确定按钮的字体大小    default 16.0f                          |
| wCancelFont                | CGFLoat      | 取消按钮的字体大小    default 16.0f               |
| wTitleFont                | CGFLoat        | 标题文本的字体大小       default 14.0f                           |
| wMessageFont                | CGFLoat        | 内容文本的字体大小     default 16.0f                        |
| wMainRadius                | CGFLoat        |弹出视图的圆角        default 15.0f                   |
| wShadowColor                | UIColor      | 遮罩层的颜色   default 0x333333            |
| wShadowAlpha                | CGFLoat        | 遮罩层的透明度   default 0.4f                        |
| wShadowCanTap                | BOOL        |  遮罩层能否点击关闭     default YES                         |
| wShadowShow                | BOOL        | 遮罩层是否显示     default YES                    |
| wEffectShow                | BOOL      |毛玻璃是否显示     default NO            |
| wMultipleSelection                | BOOL        | 多选   default NO                          |
| wSelectShowChecked                | BOOL        |选中是否打钩      default NO                 |
| wTextAlignment                | NSTextAlignment| 文本对齐方式      default center                        |

### DialogTypeAuto
| DialogTypeAuto参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wDisappelSecond                | CGFLoat        | 自动消失的时间   default  1.5f                            |

### DialogTypePay
| DialogTypePay参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wSonData                | id        | 支付方式选择数据源                         |
| wKeyBoardMarginY                | CGFLoat        | 弹窗与键盘的距离   default  70                            |
| wPayNum                | NSInteger        | 支付密码位数   default  6(若要设置位数比6大的则要保证宽度足够)                          |
| wDefaultSelectPayStr                | NSString        | 支付方式默认文本   default  农业银行                          |


### DialogTypeWrite
| DialogTypeWrite参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wPlaceholder                | NSString        | 提示语  default 请输入                       |
| wWirteTextMaxLine                | NSInteger        | 编辑框可换行的最大行数   default 7                          |
| wWirteTextMaxNum                | NSInteger        |编辑框可输入的最大数字   default   -1(-1为不限制)                   |
| wWirteKeyBoardType                | UIKeyBoardType        | 编辑框的键盘type  default  UIKeyboardTypeDefault                          |

### DialogTypePop
| DialogTypePop参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wPercentAngle                | CGFLoat        | 弹出的气泡位置  default  0.5f                         |
| wPercentOrginX                | CGFLoat        | 弹出视图的中心X轴偏移   default 1.0f (中间)                          |
| wDirection                | DiaDirection        |弹出视图的方向 default   directionDowm                  |
| wNavigationItem                | BOOL        | 导航栏位置   default  NO                          |
| wTapView                | UIView        | 触发点的视图 default  -       必传                 |
| wTapRect                | CGRect        |  如果弹出视图的frame不准确 可以自行调节   |
| wTapViewType                | DiaPopInView        | 所在父视图的类型    default normal                |
| wTapViewTableViewFoot                | BOOL        |父视图的tableviewHead还是tableviewFoot default Head           |
| wTableViewSectionHead                | NSInteger        | 在tableViewHead上的按钮所在的headViewSection的index default 0             |
| wPopViewBorderWidth                | CGFloat        | 弹窗视图的borderWidth default 0             |
| wPopViewBorderColor                | UIColor        | 弹窗视图的borderColor default 主题颜色        |
| wPopViewRectCorner                | DialogRectCorner        | 弹窗视图的圆角 可单独设置或者全部设置  默认无 和UIRectCorner用法相同 多了一个none            |

### DialogTypeDown
| DialogTypeDown参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wImageSize                | CGSize        | 图片的大小  default (50,50)                         |
| wImageName                | NSString        | 图片路径名字   default  -                        |
| wProgressTintColor                | UIColor        |进度条闲置时候的颜色 default   0xFF9900                  |
| wTrackTintColor                | UIColor        |  进度条动作时候的颜色    default  0xF3F4F6                          |

### DialogTypeMenusSelect
| DialogTypeMenusSelect参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wTableViewColor                | NSArray        |  tableview的背景颜色  default  FFFFFF/F6F7FA/EBECF0/666666

### DialogTypeLocation
| DialogTypeLocation参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wLocationType                | NSInteger        | 地区关联层级  default  3                         |
| wChainType                | ChainType        | 关联层级的样式    default  ChainPickView                        |
| wSeparator                | NSString        |选中数据的分隔符 default  ,                  |

### DialogTypeDatePicker
| DialogTypeDatePicker参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wDateTimeType                | NSString        |  时间选择器样式    yyyy年MM月dd日HH时mm分ss秒(自由组合)  default yyyy:MM:dd HH:mm:ss                       |
| wPickRepeat                | BOOL        | pickView无限循环   default  YES                        |
| wDefaultDate                | NSDate        | 默认选中时间   default  当前时间                        |


### Share/tabbarMenu/NaviMENU
| Share/tabbarMenu/NaviMENU参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wColumnCount                | NSInteger        |  列    default  -                     |
| wRowCount                | NSInteger        | 行   default  -                        |
| 注意如果设置了行和列 要如期显示 要设置好wHeight  |

### DialogTypeLoading
| DialogTypeLoading参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wLoadingType                | LoadingStyle        | 加载框样式  default  LoadingStyleWait                         |
| wLoadingSize                | CGSize        |  加载框size default  (90,90)                        |
| wLoadingColor                | UIColor        |加载框线条颜色 default  确定按钮的文本颜色                  |

### DialogTypeCardPresent
| DialogTypeCardPresent参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wOpenScrollClose                | BOOL        | 滑动到顶部继续滑动可关闭  default  YES                         |
| wLeftScrollClose                | BOOL        |  测滑可关闭 default  YES                      |
| wOpenDragging                | BOOL        |开启拖动  default  YES                  |
| wScaleParentVC                | BOOL        |缩放底部控制器 default YES                  |
| wParentHeadView                | -        |自定义顶部视图  default  -                  |
| wParentBottomView                | -        |自定义底部视图 default   -                  |

### DialogTypeCalander
| DialogTypeCalander参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wDirectionVertical                | BOOL        | 开启纵向滑动  default  NO(横向滑动)                         |
| wCalanderCanScroll                | BOOL        |  开启滑动 default  YES                      |
| wOpenChineseDate                | BOOL        |开启农历节日显示  default  YES                  |
| wHideCalanderBtn                | BOOL        |隐藏日历上的操作按钮 default YES                  |
| wDateShowCircle                | NSArray        |展示圆点的日期@[[NSDate date]]  default  -                  |
| wReginerCollectionCell                | NSString       |注册自定义的collectionViewCell default   -                  |

### DialogTypeMyView
| DialogTypeMyView参数               | 类型      | 作用   (默认值)                                 | 
|------------------------|-----------|-----------------------------------------------------|
| wAddBottomView                | BOOL        |是否添加底部按钮   default  NO                            |

### Events
| Events                | 作用   (默认值)                                 | 
|----------------------------------|-------------------------------------------|
| wEventOKFinish       |确定点击事件                             |
| wEventCancelFinish       |取消点击事件(不传默认没有取消按钮)                             |
| wEventFinish       |所有的操作事件                          |
| wEventClose       |弹窗关闭事件                           |
| wEventMenuClick       |菜单点击事件                            |
| wSelectCell       |自定义cell点击                             |
| wMyCell       |自定义cell                              |
| wMyDiaLogView       |自定义弹窗View(返回最底部的view)                         |
| wCalanderCell       |自定义日历cell                              |
| wCalanderCellClick       |自定义日历点击                              |


用法
==============

### 默认模式

      Dialog().wTypeSet(DialogTypeNornal).wStart();
    
### 多选模式

      Dialog().wTypeSet(type)
               .wEventOKFinishSet(^(id anyID, id otherData) {
                    NSLog(@"%@",anyID);
                })
                //出现动画
                .wShowAnimationSet(AninationCombineTwo)
                .wTitleSet(@"")
                .wMultipleSelectionSet(YES).wSelectShowCheckedSet(YES)
                .wDataSet(@[@"游泳",@"打篮球",@"打羽毛球",@"爬山",@"踢足球",@"乒乓球"])
                .wStart();

### 自定义弹窗(优酷) 更多自定义弹窗看demo  
    	
     Dialog()
     .wTypeSet(DialogTypeMyView)
     .wMyDiaLogViewSet(^UIView *(UIView *mainView) {
         mainView.layer.masksToBounds = YES;
         UIView *view = [[CustomView alloc] initWithFrame:CGRectMake(0, 0, 300, 250) superView:mainView];
         mainView.layer.masksToBounds = YES;
         mainView.layer.cornerRadius = 10;
         return view;
     })
     .wStart();
    
### 自定义弹窗传入实现WMZCustomPrototol协议的UIView
        
     Dialog()
     .wOpenKeyBoardSet(YES)
     .wCustomView(DemoTwoView.new)
     .wStart();
    
### 传入param

     WMZDialogParam *param = WMZDialogParam.new;
     param.wType = DialogTypeShare;
     param.wEventMenuClick = ^(id anyID, NSInteger section, NSInteger row) {
                
     };
     param.wData = @[
         @{@"name":@"微信",@"image":@"wallet"},
         @{@"name":@"支付宝",@"image":@"aaa"},
     ];
     param.wRowCount = 1;
     param.wColumnCount = 4;
     Dialog().wStartParam(param);

### 暗黑模式

    Dialog()
    .wTypeSet(DialogTypeSheet)
    .wDataSet(@[@"男",@"女",@"保密"])
    .wDarkMode(nil)
    .wStartView(self.view);

### 常见问题（开始收录）

     1 如何改变位置？
     (1) version < 1.4.2
    .wCustomMainViewSet(^(UIView *mainView) {
        CGRect rect = mainView.frame;
        rect.origin.x = 30;
        rect.origin.y = 100;
        mainView.frame = rect;
    })
     (2) version > 1.4.2 (wPoint)
    2 默认是开启横竖屏监听的如果有问题可以把wDeviceDidChange设为NO
    3 多个弹窗优先级可以设置wLevel(同个父级有效)
    4 默认弹窗wStart是在window层 如果要设置不同层可以用wStartView(传入父view)
    
     (3)///设置全局默认配置 主题色字体等 
     [WMZDialogManage settingGlobalConfig:^(WMZDialogParam * _Nullable param) {
         param.wOKColor = UIColor.redColor;
     }];



### 依赖
无任何依赖 

安装
==============

### CocoaPods  
1. 将 cocoapods 更新至最新版本.
2. 在 Podfile 中添加    pod 'WMZDialog'
3. 执行 `pod install` 或 `pod update`。
4. 导入 #import "WMZDialog.h"。


### 手动安装

1. 下载 WMZDialog 文件夹内的所有内容。
2. 将 WMZDialog 内的源文件添加(拖放)到你的工程。
3. 导入 #import "WMZDialog.h"

系统要求
==============
该库最低支持 `iOS 9.0` 和 `Xcode 9.0`。


个人主页
==============
使用过程中如果有什么bug欢迎给我提issue 我看到就会解决
[我的简书](https://www.jianshu.com/p/601ad3960353)

更新日记
==============
- 20221119 v1.4.99
- 20220929 v1.4.12 新增富文本支持 
- 20220926 v1.4.11 修复日历bug
- 20220925 v1.4.8 fix #68 #66 #60 #58 新增全局配置使用 新增多个属性
- 20211229 v1.4.6 修复崩溃 删除1.4.5 1.4.3有问题版本
- 20211018 v1.4.2 新增wPoint自定义位置
- 20210929 v1.4.0 新增暗黑模式 适配ios15 底层修改 
- 20210514 v1.3.2 修改wDidChange和wLevel默认值
- 20210513 v1.3.1 
(1)新增通用wAutoClose属性 响应库内的自动关闭 default YES 如果设为NO则需要自己调用手动关闭的类方法 closeWithshowView 
(2) writeType新增 wRegular属性  正则校验规则 default nil  例如 可传入 @{@"reguler":@"^1+[3578]+\\d{9}",@"reguletTip":@"请输入正确的手机号"}
- 20210501 v1.3.0 新增DialogTypeToast类型 修复若干问题（消除警告 建议更新至此）
- 20210412 v1.2.6 新增wLevel属性可管理多个弹窗的层级, 加入WMZDialogManage管理类
- 20210202 v1.2.5 优化LoadingType 
- 20210113 v1.2.4 优化静态库xib问题 LoadingType优化 可作为项目的loading框使用
- 20210107 v1.2.3 优化选择弹窗 解决pod里没有xib文件导致报错的问题
- 20210105 v1.2.1 日历弹窗新增多个连续区域 支持横开启屏监听wDeviceDidChange 优化列表选项
- 20201221 v1.2.0 日历弹窗新增连续区域 pop弹窗修复bug+新增自定义三角形size
- 20201218 v1.1.10 修复ios14无法弹出的问题
- 20201118 v1.1.9 新增阴影点击回调 新增自定义地区数据
- 20201009 v1.1.8 修复bug
- 20200929 v1.1.7 支持地区/拾取器/多级菜单 除了关于时间的默认选中用wDefaultDate,其他使用wListDefaultValue
- 20200920 v1.1.6 适配ios14 
- 20200828 v1.1.5 新增列表默认选中的属性
- 20200606 v1.1.3 新增wTag可防止重复点击 新增自定义frame的方法
- 20200519 v1.1.2 优化一些地方
- 20200117 v1.1.0 更新一波bug
- 20200107 v1.0.7 修复bug
- 20191225 v1.0.6 优化日期选择弹窗类型 
- 20191223 优化pop弹窗类型 支持圆角的定制 支持tableview等滚动视图的弹出
- 20191216 v1.0.5 修复ios10崩溃问题
- 20191214 v1.0.4 修复ios9.0某个type闪退问题和增加normalType确定或取消文字过多自动换行
- 20191124 v1.0.3 修复pod 版本过低导致出现weak的问题
- 20191113 v1.0.2 修复pod指定ios版本的问题
- 20191109 v1.0.1
- 20191112 新增wDefaultDate属性  表示默认选中时间 default 当前时间
- 20191108 新增ios13 present弹窗
- 20191107 新增日历弹窗
- 20191105 修改自动消失的样式 可支持图文
- 20191005 优化代码修复地区弹窗bug
