javascript中存储对象都是存地址的，所以浅拷贝是都指向同一块内存区块，而深拷贝则是另外开辟了一块区域

Object.assign() 只是一级属性复制，比浅拷贝多深拷贝了一层而已。用的时候，还是要注意这个问题的。

ex1:
```javascript
const defaultOpt = {
    title: {
        text: 'hello world',
        subtext: 'It\'s my world.'
    }
};

const opt = Object.assign({}, defaultOpt, {
    title: {
        subtext: 'Yes, your world.'
    }
});

console.log(opt);

// 预期结果
{
    title: {
        text: 'hello world',
        subtext: 'Yes, your world.'
    }
}
// 实际结果
{
    title: {
        subtext: 'Yes, your world.'
    }
}
```
深拷贝的简单实现

```javascript
const obj1 = JSON.parse(JSON.stringify(obj));
```
