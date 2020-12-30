### eslintrc.js配置
```
module.exports = {
  // 告诉eslint找当前配置文件不能往父级查找
  root: true,
  // 解析器配置
  parserOptions: {
    // 指定eslint解析器的，解析器必须符合规则，babel-eslint解析器是对babel解析器的包装使其与ESLint解析
    parser: 'babel-eslint', 
    // 支持es6语法，但并不意味着同时支持新的 ES6 全局变量或类型（比如 Set 等新类型）
    ecmaVersion: 6,
    // 指定来源的类型，'script' (默认) 或 'module'（如果你的代码是 ECMAScript 模块)
    sourceType: 'module', 
    //指定要使用其他那些语言对象
    ecmaFeatures: {
      jsx: true, //启用jsx语法
    } 
  },
  // 指定环境的全局变量，下面的配置指定为浏览器环境
  env: {
    node: true,  //Node.js全局变量和Node.js范围。
  },
  // 共享配置
  // 'extends':['@vue/standard','plugin:vue/essential','plugin:vue/recommended'],
  extends: ["vue", "plugin:vue/recommended", 'prettier', 'eslint:recommended'],
  rules: {
    'block-spacing': [0], // 如果代码块是单行的时候，代码块内部前后需要留一个空格[2,"always"],
    'no-mixed-operators':0, // 运算符的eslint：不要&& ||混着写
    'vue/no-unused-components':0,//引用组建不使用就会报错
    'vue/no-use-v-if-with-v-for': 0, //不建议v-if和v-for同时使用
    'vue/require-default-prop':'off', //props必须规定default选项
    'vue/max-attributes-per-line':['error',{
      'singleline':3,
      'multiline':{
        'max':1,
        'allowFirstLine':true,
      },
    }],
    'vue/html-indent':['warn',2,{
      'alignAttributesVertically':false,
    }],
    // 组件名大小写
    "vue/component-name-in-template-casing": ["error", "kebab-case", {
      "registeredComponentsOnly": false,
      "ignores": []
    }],
    'vue/html-self-closing':'off',
    'generator-star-spacing':'off', // generator函数中星号两边的空白。
    'perfer-promise-reject-errors':['off',{
      allowEmptyReject: true
    }],
    // 开发模式允许使用console
    'no-console': process.env.NODE_ENV === 'production' ? 'error' : 'off',
    // 开发环境允许使用调试 (生产模式禁用)
    'no-debugger': process.env.NODE_ENV === 'production' ? 'error' : 'off',
    'semi':['error','never'], //不加分号  "semi": [2,"always"],//加分号
    'linebreak-style':[0,'error','windows'],
    'eol-last':'off',
    'comma-dangle':['error','always-multiline'],  //在定义对象或数组时，最后一项不能加逗号 [2,"never"],
    "new-cap": [2,{'newIsCap': true,'capIsNew': false}], //构造函数首字母大写
    "no-class-assign": 2, //禁止覆盖class命名，也就是说变量名不要和class名重名
    // "arrow-spacing": [2,{"before": true,"after": true}], //箭头函数中的箭头前后需要留空格
  }
}
```
