# 电力系统时序运行模拟

该项目实现了一个完整的电力系统时序运行模拟框架，包含传统机组组合模型(TUC)、频率约束机组组合模型(FDUC)和增强型频率约束机组组合模型(CCFDUC)的对比分析。

## 功能特性

- 多种机组组合优化模型的实现与对比
- 可再生能源发电模拟
- 频率响应分析
- 系统运行成本计算
- 完整的数据可视化支持

## 环境要求

- Julia 1.x
- 必需的包依赖：
  - JuMP：优化建模
  - Gurobi：求解器
  - Plots：绘图支持
  - PlotlyJS：交互式绘图
  - DataFrames：数据处理
  - LaTeXStrings：LaTeX 公式支持
  - 其他辅助包：Revise, Test, DelimitedFiles, Clustering, StatsPlots

## 安装说明

1. 克隆项目到本地：

````bash
git clone https://github.com/yuanyipeng0/nsfc_2025.git
``

## 项目结构
Julia_SequentialOperationSimulation/
├── src/
│   ├── formatteddata.jl              # 数据格式化
│   ├── renewableenergysimulation.jl  # 可再生能源模拟
│   ├── SUCuccommitmentmodel.jl       # 传统机组组合模型
│   ├── FCUCuccommitmentmodel.jl      # 频率约束机组组合模型
│   ├── enhance_FCUCuccommitmentmodel.jl  # 增强型频率约束模型
│   └── ...
├── mainfun.jl                        # 主程序入口
└── README.md
Julia_SequentialOperationSimulation/
├── src/
│   ├── formatteddata.jl              # 数据格式化
│   ├── renewableenergysimulation.jl  # 可再生能源模拟
│   ├── showboundrycase.jl           # 边界条件展示
│   ├── readdatafromexcel.jl         # Excel数据读取
│   ├── SUCuccommitmentmodel.jl      # 传统机组组合模型
│   ├── FCUCuccommitmentmodel.jl     # 频率约束机组组合模型
│   ├── enhance_FCUCuccommitmentmodel.jl # 增强型频率约束模型
│   ├── creatfrequencyconstraints.jl # 创建频率约束
│   ├── BFLib_consideringFRlimit.jl  # 频率响应限制基础函数库
│   ├── new_BFLib_consideringFRlimit.jl # 新版频率响应限制函数库
│   ├── casesploting.jl             # 案例绘图
│   ├── saveresult.jl               # 结果保存
│   ├── generatefittingparameters.jl # 生成拟合参数
│   ├── draw_onlineactivepowerbalance.jl # 绘制在线有功功率平衡
│   ├── cal_Diffaggregatedfrequencyparameters.jl # 计算聚合频率参数
│   └── draw_addditionalpower.jl    # 绘制额外功率
├── mainfun.jl                      # 主程序入口
└── README.md                       # 项目说明文档

## 使用说明

1. 运行主程序：
```julia
include("mainfun.jl")

这份 README 文档包含了项目的主要信息，包括功能特性、环境要求、安装说明、项目结构、使用方法等关键内容。您可以根据实际需求对其进行修改和补充。

建议您补充以下信息：
1. 项目的具体仓库地址
2. 选择合适的开源许可证
3. 添加您的联系方式
4. 补充更详细的使用示例
5. 添加具体的结果图表示例
````
