# Entry Component(app.module.ts)

When we dont specify selecter in any html files we have to include the component name in entrycomponent .

# bootstrap(app.module.ts)

To let angular know this is entry point of application, can be done through ngDoBootstrap function also.

# Shadow DOM

Used for specifying encapsulating styles respective to component or document

1. ViewEncapsulation.None - No Shadow DOM at all. Therefore, also no style encapsulation.

- Updates style in document head with style name directly

```
    <html>
<head>
<style>
  .zippy {
    background: green;
  }
</style>
</head>
<body>

```

2. ViewEncapsulation.Emulated - No Shadow DOM but style encapsulation emulation.

   - Updates style in document head with style name and component information

```
  <head>
  <style>
  .zippy[_ngcontent-1] {
  background: green;
  }
  </style>
  </head>

```

3. ViewEncapsulation.Native - Native Shadow DOM with all it’s goodness.

   - uses native shadow DOM directly

```
    <my-zippy title="Details">
    #shadow-root
    | <style>
    |   .zippy {
    |     background: green;
    |   }
    | </style>
    | <div class="zippy">
    |   <div (click)="toggle()" class="zippy__title">
    |     ▾ Details
    |   </div>
    |   <div [hidden]="!visible" class="zippy__content">
    |     <content></content>
    |   </div>
    | </div>
    "This is some content"
    </my-zippy>

```
