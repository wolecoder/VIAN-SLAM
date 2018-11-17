### git的使用方法 (ubuntu)

#### 一 、下载git

```Linux
sudo apt-get install git
```

#### 二、进行git配置 -- 设置用户名和邮箱

```git
git config --global user.name "username"
git config --global user.email "email address"
```

#### 三、将git和github连接起来

1. 获取ssh秘钥 -- 得到id_rsa.pub文件

   ```git
   ssh-keygen -C 'email address' -t rsa
   ```

2. 在github中的setting中的SSH and GPG keys中的New SSH key填写获取到的秘钥, 即<id_rsa.pub>中的奇怪字串

3. 至此, git和github已经连接起来

#### 四、将github上的文件pull到本地

1. 准备条件: 首先本地仓库和github上的某个想要的仓库建立联系

   ```git
   ① 本地文件夹中执行 git init
   ② git remote add origin <wanted project URL>
   for example:
   <wanted project URL>: https://github.com/wolecoder/VIAN-SLAM.git
   ```

2. 将github上想要仓库的文件pull到本地

   ```git
   git pull origin master
   ```

#### 五、本地文件push到github

```git
① 单个文件: git add <filename>  所有文件: git add .
② git commit -m '<description>'
③ git push origin master
④ input github username: <github's username>
⑤ input github password: <github's password>
```

#### END -- git的一些常用命令

```git
git init
```

```git
git status
```

```git
git add
```

``` git
git commit -m '<infomation for this commit>'
```

```git
git log
```

```
git branch
```

```git
git checkout <another branch>
```

```git
git merge
```

```git
git branch -d <branch name>
```

```git
git branch -D <branch name>
```

```git
git tag
```



