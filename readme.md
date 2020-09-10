当在一台机器上编辑完blog文档之后，复制hexo项目下的本地文件，到备份的项目下，用于同步两台设备的本地文件。否则，在机器B上本地内容较少，提交blog之后会覆盖在机器B上已经提交的blog内容。  
### 具体步骤：
1. 在机器A上生成并部署新的blog到github
2. 复制机器A上的hexo项目本地文件到备份项目之下，然后将备份项目提交到github
3. 在机器B创建新的blog之前，先同步github上的备份项目到本地的备份项目
4. 然后将同步下来的文件复制到机器B的hexo项目下
5. 在机器B上生成并部署新的blog到github
6. 复制机器B上的hexo项目本地文件到备份项目之下，然后将备份项目提交到github
 
文件夹：scaffolds、source、themes  
文件：_config.yml、package.json、.gitignore  