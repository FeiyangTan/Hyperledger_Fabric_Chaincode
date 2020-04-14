# 共享资产平台需求整理
## fabric 1.4

## 功能整理
* 用户开户&销户
* 资产登记&注销
* 资产转移
* 查询用户
* 查询资产
* 查询资产转移记录


## 实体

### 用户
* 名字
* 用户id
* 资产列表

### 资产
* 名字
* 资产id
* 信息
* 所属用户id
* 原始所属用户

### 资产转移记录
* 资产id
* 拥有者 （首次登记为null）
* 新拥有者


## 交互

### 添加用户
* 输入：名字，用户id
* 添加新用户

### 用户注销
* 输入：用户id
* 用户注销
* 用户所拥有的资产注销

### 添加资产
* 输入：名字，资产id，信息，拥有者
* 添加资产
* 更新资产拥有者资产列表
* 添加资产转移历史

### 资产注销
* 输入：资产id
* 更新资产拥有者资产列表
* 资产注销
* 添加资产转移历史

### 资产转移
* 输入：资产id，拥有者，接收者
* 添加资产转移历史

## 查询

### 用户查询
* 输入：用户id
* 输出：用户

### 资产查询
* 输入：资产id
* 输出：资产

### 查询资产转移记录
* 输入：资产id
* 输出：资产转移记录