下载仓库后，只需要三步就能恢复环境：

1. 创建并激活 venv 虚拟环境
2. `pip install -r requirements.txt`
3. `scons build/ALL/gem5.opt -j$(nproc)`

# 1. 在gem5根目录创建虚拟环境文件夹
`python3 -m venv venv_gem5`

# 2. 激活虚拟环境
`source venv_gem5/bin/activate`

# 3. 此时再安装依赖，不会报任何系统环境限制
`pip install -r requirements.txt`

# 4. 装完重新执行scons编译
`scons build/ALL/gem5.opt -j$(nproc)`
这一步需要等10~20分钟

# 运行测试代码
`build/ALL/gem5.opt configs/learning_gem5/part1/simple.py`
