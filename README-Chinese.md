# xcode-snippet-templete
Xcode中快捷创建的代码块与默认生成类的模板

## snippet
将`CodeSnippets`放入`/Users/用户名/Library/Developer/Xcode/UserData/CodeSnippets`文件夹中。
代码块都是以`@`开头（例如：@property (nonatomic, strong) UILabel xxLabel; 输入@l就可以显示）

### 属性创建
#### 支持UI属性创建：
- UIView(@View)
- UILabel(@Label)
- UIButton(@Button)
- UIImageView(@ImageView)
- UIStackView(@StackView)
- UITableView(@TableView)
- UICollectionView(@CollectionView)

#### 支持成员变量属性创建：
- strong(@strong)
- weak(@weak)
- assign(@assign)
- copy(@copy)

### 常用代理或数据源方法创建
- UITableViewDelegate(@DelegateTableView)
- UICollectionViewDelegate(@DelegateCollectionView)

### 懒加载
- UIView(@LazyView)
- UILabel(@LazyLabel)
- UIButton(@LazyButton)
- UIImageView(@LazyImageView)
- UIStackView(@LazyStackView)
- UITableView(@LazyTableView)
- UICollectionView(@LazyCollectionView)

### 快捷初始化
#### View
- initView(@initView)
```
- (instancetype)init {
    self = [super init];
    if (self) {
        [self subviewsInitialization];
        [self subviewsConstraint];
    }
    return self;
}

#pragma mark Configure Views

- (void)subviewsInitialization {
    
}

- (void)subviewsConstraint {
    
}
```

- initView(@initViewFrame)
```
- (instancetype)initWithFrame:(CGRect)frame {
    self = [super initWithFrame:frame];
    if (self) {
        [self subviewsInitialization];
        [self subviewsConstraint];
    }
    return self;
}

#pragma mark Configure Views

- (void)subviewsInitialization {
    
}

- (void)subviewsConstraint {
    
}
```

- initTableViewCell(@InitTableViewCell)
```
- (instancetype)initWithStyle:(UITableViewCellStyle)style reuseIdentifier:(NSString *)reuseIdentifier {
    self = [super initWithStyle:style reuseIdentifier:reuseIdentifier];
    if (self) {
        self.selectionStyle = UITableViewCellSelectionStyleNone;
        self.contentView.backgroundColor = [UIColor whiteColor];
        [self subviewsInitialization];
        [self subviewsConstraint];
    }
    return self;
}

#pragma mark Configure Views

- (void)subviewsInitialization {
    
}

- (void)subviewsConstraint {
    
}
```

## templete
将`Templates`放入`/Users/用户名/Library/Developer/Xcode/`文件夹中如果存在就将里面的文件复制进入即可。
模板中包含了默认初始化，代码分层等，可以根据自己需要进行修改。
使用时示例图：
![Templates](https://z3.ax1x.com/2021/09/28/4f1Ajs.png)

其他贴图：
![UIViewController](https://z3.ax1x.com/2021/09/28/4f17bq.jpg)
![UIView](https://z3.ax1x.com/2021/09/28/4f3PVx.jpg)
