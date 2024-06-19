release使用

- 本地验证releaser配置是否有误
```
goreleaser release --snapshot --clean
```

- 校验.releaser.yaml正确性
```
goreleaser check
```

- 如果需要发布到公开的镜像仓库需要暴露相关token信息
```
export GITHUB_TOKEN="YOUR_GH_TOKEN"
```

- 为代码仓库添加tag信息
```
git tag -a v0.1.0 -m "First release"
git push origin v0.1.0
```

- 执行发布命令
```
goreleaser release
```
