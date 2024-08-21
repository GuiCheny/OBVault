
## conda指令

- 更新conda:conda update conda
- 查看环境列表:conda env list/conda info --env/--ec
- 创建环境:conda create --name myenv
- 克隆环境:conda create -n env2 --clone env1 克隆env1
- 删除环境:conda remove -n env1 --all
- 激活环境:conda activate xx
- 失活环境:conda deactivate
- 查看安装包列表:conda list
- 查找某软件包:conda search ..
- 软件包安装:conda install ..
- 软件包安装（txt文件）:conda install --file packages.txt
- 更新已安装的软件包:conda update --all
- 删除某软件包:conda remove package_name
- 查看路径（镜像）:conda config --show channels
- 配置增加路径:conda config --add channels url..
- 配置删除路径:conda config --remove channels url

## pip和conda在安装软件包时主要有以下区别

- 源不同
  pip主要使用Python Package Index（PyPI）作为软件包的安装源，而conda则使用Anaconda存储库作为其安装源。Anaconda存储库是一个经过精心策划的存储库，专门用于支持科学计算和数据科学领域的软件包。
- 可安装的软件包范围不同
  pip主要是用于安装和管理Python库，而conda不仅可以安装Python库，还可以安装一些依赖的C/C++库或其他语言库。
- 依赖处理方式不同
  pip在安装库时，是按顺序一个个检查依赖，如果安装的库之间存在不兼容的依赖，可能会导致安装失败。而conda在执行命令时会统一检查所需安装的库的兼容性，以安装最合适的版本。
  因此，在选择使用pip还是conda进行软件包的安装时，需要根据具体的需求和环境来决定。
