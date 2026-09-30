## 1.6.3

- 修 A 端「错误接口令牌被分发到 Keystore maintenance 事务」：只有调用方是平台进程时才按 maintenance 解析，别的进程发同名字符串不再被拦断
- 修「用户认证授权列表检测未完成 / 用户认证策略检测未完成」：502-509 认证条目随远端认证请求带走，证书里不再出现「建钥要认证、证书写 NO_AUTH_REQUIRED」自相矛盾
- 修锁屏后热替换导致认证建钥一律回锁屏状态：解锁材料落到 /data/misc/keystore/ommega/unlock.state，重启后自动恢复
- 认小米那套 HIDL SOTER 服务，小米机型也能拦
- 认证请求带上本机 KeyMint 版本，开机按配置声明补丁级别与 vbmeta 信任根
- 构建脚本支持多 ABI 并行
