# -import numpy as np
from scipy.stats import entropy

# 定义联合分布
joint_distribution = np.array([
    [0.125,0.0625,0.03125,0.03125],
    [0.0625,0.125,0.03125,0.03125],
    [0.0625,0.0625,0.0625,0.0625]
    [0.25,0,0,0]
])

# 计算联合概率分布
total = np.sum(joint_distribution)
joint_prob = joint_distribution / total

# 计算信息熵
joint_entropy = entropy(joint_prob.flatten(), base=2)

print(f"信息熵: {joint_entropy}")
