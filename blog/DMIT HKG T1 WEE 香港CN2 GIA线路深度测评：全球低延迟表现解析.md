# DMIT HKG T1 WEE 香港CN2 GIA线路深度测评：全球低延迟表现解析

## 全球节点延迟实测
| 测试节点         | 延迟(ms) |
|------------------|---------|
| 中国台湾         | 14      |
| 韩国首尔         | 36      |
| 新加坡           | 37      |
| 日本东京         | 48      |
| 印尼雅加达       | 48      |
| 阿联酋迪拜       | 122     |
| 美国圣何塞       | 157     |
| 俄罗斯莫斯科     | 155     |
| 德国法兰克福     | 165     |
| 英国伦敦         | 175     |
| 法国巴黎         | 176     |
| 印度孟买         | 180     |
| 智利圣地亚哥     | 345     |

👉 [【推荐收藏】2025年 DMIT 最新优惠活动整理汇总 - 每日更新可用优惠套餐](https://bit.ly/dmit_coupon)

## 硬件性能测试
bash
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #
#              Yet-Another-Bench-Script              #
#                     v2023-04-23                    #
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #

处理器：AMD EPYC 7402P 24-Core @ 2.79GHz
内存：461.3 MiB | 虚拟化：KVM
磁盘读写（混合R/W）：
4K性能：21.28 MB/s（5.3k IOPS）
1M性能：606.72 MB/s（591 IOPS）

IPv4网络吞吐量：
洛杉矶节点：上行455Mbps/下行426Mbps
巴黎节点：上行706Mbps/下行548Mbps
塔什干节点：上行615Mbps/下行507Mbps

## 三网回国路由解析
text
电信163线路：北京/广州/成都节点稳定连接
联通4837线路：全国主要城市低延迟接入
移动CMI线路：全程直连无绕行
上海电信节点：存在部分测试超时情况
教育网节点：未发现特殊路由优化

## 深度速度测试报告
### 单线程下载峰值
text
移动成都节点：下行69.7Mbps/上行90.3Mbps
联通上海5G节点：下行42.3Mbps/上行52.4Mbps 
电信上海节点：存在断流现象（建议优化TCP配置）

### bench.sh全球测速
text
国际带宽表现：
东京节点：下行1561Mbps/上行389Mbps
阿姆斯特丹节点：下行992Mbps/上行383Mbps
洛杉矶节点：下行1029Mbps/上行218Mbps

大中华区连接：
香港节点：延迟仅1.18ms（CN2 GIA线路优势）
上海节点：下行528Mbps（受国际出口限制）

## 技术亮点总结
1. **网络架构优势**：采用CN2 GIA三网优化线路，中国大陆访问质量显著优于普通BGP线路
2. **硬件配置亮点**：AMD EPYC 7402P处理器配合NVMe存储方案，IO性能达600+ MB/s
3. **全球互联能力**：洛杉矶、东京等核心节点实现500Mbps+双向传输
4. **路由优化方案**：移动CMI/联通4837直连，有效降低跨国访问延迟

> 测试环境说明：所有数据采集自Debian 11系统，测试期间未启用SWAP空间，实际使用建议配置1GB以上内存