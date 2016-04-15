# Angular 2 實戰

### 目錄
* [快速入門](#快速入門)
* [元件](#元件)
* [內建指令](#內建指令)
* [表單與輸入](#表單與輸入)
* [路由與導覽列](#路由與導覽列)
* [指令](#指令)
* [生命週期掛鉤](#生命週期掛鉤)
* [管道](#管道)
* [服務](#服務)
* [伺服器通訊](#伺服器通訊)

***

### 快速入門
```ts
// basic-app.ts
import { Component } from 'angular2/core';

@Component({
  selector: 'basic-app',
  template: `
    <p>Hello {{ 1 + 1 }}</p>
  `
})
export class BasicAppComponent { }
```
`{{}}`表達式
```ts
// hello-world.ts
import { Component } from 'angular2/core';

@Component({
  selector: 'hello-world',
  template: `
    <input type="text" [(ngModel)]="yourName" placeholder="輸入您的姓名">
    <p>Hello {{ yourName }}</p>
  `
})
export class HelloWorldComponent {
  public yourName: string = '';
}
```
`[]`綁定　`()`事件

### 元件
```ts
// click-me.ts
import { Component } from 'angular2/core';

@Component({
  selector: 'click-me',
  template: `
    <button (click)="onClickMe()">點擊我</button>
    <p>{{ clickMessage }}</p>
  `
})
export class ClickMeComponent {
  public clickMessage: string = '';
  onClickMe() {
    this.clickMessage = 'Hello Angular 2';
  }
}
```
```ts
// add-item.ts
import { Component } from 'angular2/core';

@Component({
  selector: 'add-item',
  template: ``
})
export class AddItemComponent {
  public list: string[] = ['Angular', 'Material', 'Firebase'];  // 預設的清單
  addItem(newItem: string) {
    if (newItem) {  // 防止無輸入的狀態下新增項目
      this.list.push(newItem);
    }
  }
}
```


### 內建指令

### 表單與輸入

### 路由與導覽列

### 指令

### 生命週期掛鉤
元件與指令
* ngOnInit
* ngOnChanges
* ngDoCheck
* ngOnDestroy

### 管道

### 服務

### 伺服器通訊
