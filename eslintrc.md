```
module.exports = {
  env: {
    browser: true,
    // 'es2021': true, 暂时不允许使用
    node: true
  },
  extends: [
    'eslint:recommended',
    'plugin:vue/essential',
    '@vue/standard'
  ],
  parserOptions: {
    parser: 'babel-eslint',
    ecmaVersion: 10, // 必须是10以下包括10
    sourceType: 'module'
  },
  plugins: [
    'vue',
  ],
  rules: {
    'quotes': ['error', 'single'],
    // 分号
    'semi': ['error', 'never'],
    'block-spacing': [0], // 如果代码块是单行的时候，代码块内部前后需要留一个空格[2,"always"],
    'no-mixed-operators': 0, // 运算符的eslint：不要&& ||混着写
    'vue/no-unused-components': 0, // 引用组建不使用就会报错
    'vue/no-use-v-if-with-v-for': 0, // 不建议v-if和v-for同时使用
    'vue/require-default-prop': 'off', // props必须规定default选项
    'vue/max-attributes-per-line': ['error', {
      singleline: 3,
      multiline: {
        max: 1,
        allowFirstLine: true,
      },
    }],
    'no-multiple-empty-lines': [2, { max: 1 }],
    'vue/html-indent': ['warn', 2, {
      alignAttributesVertically: false,
    }],
    // 组件名大小写
    'vue/component-name-in-template-casing': ['error', 'kebab-case', {
      registeredComponentsOnly: false,
      ignores: []
    }],
    'vue/html-self-closing': 'off',
    'generator-star-spacing': 'off', // generator函数中星号两边的空白。
    'perfer-promise-reject-errors': ['off', {
      allowEmptyReject: true
    }],
    // 开发模式允许使用console
    'no-console': process.env.NODE_ENV === 'production' ? 'error' : 'off',
    // 开发环境允许使用调试 (生产模式禁用)
    'no-debugger': process.env.NODE_ENV === 'production' ? 'error' : 'off',
    'eol-last': 'off',
    // 'comma-dangle':['error','always-multiline'],  //在定义对象或数组时，最后一项不能加逗号 [2,"never"],
    'comma-dangle': 0,
    'new-cap': [2, { newIsCap: true, capIsNew: false }], // 构造函数首字母大写
    'no-class-assign': 2, // 禁止覆盖class命名，也就是说变量名不要和class名重名
    'linebreak-style': [0, 'error', 'windows'],
  }
}
```
