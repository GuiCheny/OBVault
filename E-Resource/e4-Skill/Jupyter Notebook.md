# Jupyter Notebook

## 内核切换

1. 切换到创建的虚拟环境:`conda activate {conda name}`
2. 安装ipykernel:`conda install ipykernel`
3. 设置kernel:`ipython kernel install --user --name={kernel_name}` //--user表示当前用户，kernel_name为虚拟环境名称

##  删除内核

1. 列出所有已安装的内核:`jupyter kernelspec list`
2. 删除内核:`jupyter kernelspec uninstall {kernel_name}`
