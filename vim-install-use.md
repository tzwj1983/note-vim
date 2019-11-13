# 下载地址 
官网：[下载地址](https://www.vim.org/download.php)  
```
https://www.vim.org/download.php
```
Github:[下载地址](https://github.com/vim/vim)
```
https://github.com/vim/vim
```


# 插件安装
## 插件管理器 Vundle
详见Github [地址](https://github.com/VundleVim/Vundle.vim)
```
https://github.com/VundleVim/Vundle.vim
```
###  mac或linux环境
1、 初始安装 Vundle：
```
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
2、 配置插件 :
```
set nocompatible              " 去除VI一致性,必须
filetype off                  " 必须

" 设置包括vundle和初始化相关的runtime path
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

" 让vundle管理插件版本,必须
Plugin 'VundleVim/Vundle.vim'


" 你的所有插件需要在下面这行之前
call vundle#end()            " 必须
filetype plugin indent on    " 必须 加载vim自带和插件相应的语法和文件类型相关脚本
" 忽视插件改变缩进,可以使用以下替代:
"filetype plugin on
"
" 简要帮助文档
" :PluginList       - 列出所有已配置的插件
" :PluginInstall    - 安装插件,追加 `!` 用以更新或使用 :PluginUpdate
" :PluginSearch foo - 搜索 foo ; 追加 `!` 清除本地缓存
" :PluginClean      - 清除未使用插件,需要确认; 追加 `!` 自动批准移除未使用插件
```
3、安装插件:
- 运行 vim 再运行 :PluginInstall
- 通过命令行直接安装 vim +PluginInstall +qall

### windows环境
1、 初始安装 Vundle：
```
cd %USERPROFILE%

git clone https://github.com/VundleVim/Vundle.vim.git %USERPROFILE%/.vim/bundle/Vundle.vim

gvim .vimrc
```
2、 配置插件 :
```
set nocompatible              " 去除VI一致性,必须
filetype off                  " 必须

" 设置包括vundle和初始化相关的runtime path
set rtp+=$HOME/.vim/bundle/Vundle.vim/
call vundle#begin('$HOME/.vim/bundle/')

" 让vundle管理插件版本,必须
Plugin 'VundleVim/Vundle.vim'


" 你的所有插件需要在下面这行之前
call vundle#end()            " 必须
filetype plugin indent on    " 必须 加载vim自带和插件相应的语法和文件类型相关脚本
" 忽视插件改变缩进,可以使用以下替代:
"filetype plugin on
"
" 简要帮助文档
" :PluginList       - 列出所有已配置的插件
" :PluginInstall    - 安装插件,追加 `!` 用以更新或使用 :PluginUpdate
" :PluginSearch foo - 搜索 foo ; 追加 `!` 清除本地缓存
" :PluginClean      - 清除未使用插件,需要确认; 追加 `!` 自动批准移除未使用插件
```
3、安装插件:
- 运行 vim 再运行 :PluginInstall
- 通过命令行直接安装 vim +PluginInstall +qall

### 添加插件
安装插件的命令放在vundle#begin和vundle#end之间
#### 安装完成后，到安装目录下查看使用说明  
#### 常用插件:
1、NERDTree是一个用于浏览文件系统的树形资源管理外挂,它可以让你像使用Windows档案总管一样在VIM中浏览文件系统并且打开文件或目录。
```
Bundle 'scrooloose/nerdtree'
let NERDTreeWinPos='right'
let NERDTreeWinSize=30
map <F2> :NERDTreeToggle<CR>
```