# skipper-qiniu-qn
使用了[qn](https://github.com/node-modules/qn)替代官方SDK。

**WARNING!! 请立即更新至1.1.1及以上版本来避免可能的致命错误。**

**WARNING!! Please update to 1.1.1 or higher version to avoid an critical error.**
## Examples

```Javascript
req.file('avatar').upload({
  adapter: require('skipper-qiniu-qn'),
  bucket: 'development', // required
  accessKey: 'your qiniu accessKey', // required
  secretKey: 'your qiniu secretKey', // required
}, function(err, files) {
  if (err) {
    return res.serverError(err);
  }

  return res.json({
    message: files.length + ' file(s) uploaded successfully!',
    files: files
  });
});
```

注意：暂不支持自定义policy。
