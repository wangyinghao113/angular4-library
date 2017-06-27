# angular4-library
angular2/4 开发中如何使用第三方库

#### 用第三方库

1，去[这里](https://microsoft.github.io/TypeSearch/)搜索定义文件，然后使用npm安装

2，在需要地方引入定义文件，例如：dialog.component.ts 要使用jquery，那么源码如下
```typescript
/// <reference path="../../../../node_modules/@types/jquery/index.d.ts" />
import { Component } from '@angular/core';
@Component({
    selector: 'dialog-model'
})
export class DialogComponent {
    show(){
        // 这里就可以使用jquery了
        $('#div1').show();
    }
}
```
3，在gulpfile.js里打包配置并编译
