# Text-Analysis-of-Online-Reviews-of-Scenic-Spots-and-Hotels
This is a text analysis of online reviews of scenic spots and hotels. 

这是关于景区和酒店的网评文本分析。

## Introduction 项目背景
The goal of this project is to analyze tourist review texts from 50 scenic spots and 50 hotels, enabling local cultural and tourism authorities, as well as tourism-related businesses, to better understand the real needs of tourists and improve their satisfaction.  

本项目的目标是对50个景区和50家酒店的游客评论文本进行分析，方便当地文旅主管部门和旅游相关企业了解游客的真实需求，提高游客满意度。

## Methodology 方法步骤
### 1. Impression Analysis of Scenic Spots and Hotels 景区及酒店印象分析

Used **jieba** library in Python, segmented the review texts and calculated word frequency. Applied Newton’s Law of Cooling to determine word popularity, selecting the **top 20 most popular words** for each destination.  

运用 Python 中的 **jieba** 库对评论文本进行分词处理，统计词频，并引入牛顿冷却定律计算词语热度，选取出每个目的地 TOP20 热门词。

### 2. Comprehensive Evaluation of Scenic Spots and Hotels 景区及酒店的综合评价

Built **LDA topic model** to classify reviews into five categories: service, location, facilities, cleanliness and cost-effectiveness. Then performed **sentiment analysis** to score each category. Finally, used **fuzzy comprehensive evaluation method** to obtain an overall rating for each scenic spot and hotel.  

建立 **LDA 主题模型**，将评论分为服务、位置、设施、卫生、性价比5类。运用**情感分析**得到评论对每一类别的打分。之后运用**模糊综合评价法**得到每个景区、酒店的综合评价得分。

### 3. Validity Analysis of Online Reviews 网评文本的有效性分析

To identify reviews that are irrelevant, copied, or lack meaningful content, the following validity checks are performed.

1. **Detection of repetitive reviews:** Used **cosine similarity** to quantify similarity and flagged highly similar reviews.  
2. **Identification of irrelevant or uninformative reviews:** Applied **LDA topic model** and set reviews with low topic contribution as invalid.  
3. **Short review filtering:** Reviews with fewer than five characters were set as invalid.  

为了识别内容不相关、简单复制修改和无有效内容等评论，本文对评论文本进行了有效性分析。

（1）针对简单重复类评论，本文运用**余弦相似度**对评论的相似性进行量化，识别出相似度过高的评论；

（2）针对内容无关或无有效内容的情况，本文运用前文建立的 **LDA 主题模型**，将对主题的贡献度较低的评论视为无效评论；

（3）针对文本过短的评论，统计文本长度低于 5 个字符的评论。

### 4. Feature Analysis of Scenic Spots and Hotels 景区及酒店的特色分析

Based on the comprehensive evaluation results, we categorized scenic spots and hotels into high, medium, and low levels. For each level, three scenic spots and three hotels are selected. We used **TF-IDF algorithm** to extract key features from reviews, analyzing the unique highlights of each scenic spot and hotel.

根据综合评价的结果，将景区和酒店分为高、中、低三个层次。然后，在每个层级中选取3家景点和3家酒店，运用 **TF-IDF 算法**提取特色评论，分析景区和酒店的亮点。


