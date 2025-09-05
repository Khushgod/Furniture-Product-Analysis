# Furniture-Product-Analysis
# 🛋️ Furniture Dataset Analysis Pipeline

A comprehensive data analytics pipeline for furniture e-commerce businesses to analyze product performance, pricing strategies, sales patterns, and customer segmentation.

## 📊 Overview

The **Furniture Analysis Pipeline** is a Python-based analytical framework designed to provide deep insights into furniture e-commerce data. It processes product information including titles, pricing, sales data, and tags to generate actionable business intelligence through statistical analysis, machine learning, and data visualization.

## ✨ Key Features

- **📈 Comprehensive Data Exploration**: Automated data quality assessment, missing value detection, and statistical summaries
- **💰 Pricing Strategy Analysis**: Discount categorization, price tier distribution, and revenue impact analysis
- **🎯 Sales Performance Metrics**: Top-performing product identification, sales categorization, and revenue analysis
- **🏷️ Product Categorization**: Automated furniture type classification and market share analysis
- **🔖 Tag Impact Analysis**: Statistical analysis of product tags' effect on sales performance
- **🔗 Correlation Analysis**: Relationship discovery between pricing, discounts, and sales metrics
- **🤖 Predictive Modeling**: Machine learning models for sales forecasting using Linear Regression and Random Forest
- **👥 Customer Segmentation**: K-means clustering for product segmentation and targeted recommendations
- **📊 Data Visualizations**: Comprehensive charts and graphs for visual insights
- **📋 Executive Summary**: Strategic recommendations and key performance indicators

## 🛠️ Technologies Used

- **Python 3.7+**
- **Data Analysis**: pandas, numpy
- **Visualization**: matplotlib, seaborn, plotly
- **Machine Learning**: scikit-learn
- **Statistics**: scipy.stats
- **Text Processing**: re, collections

## 📦 Installation

### Prerequisites

Ensure you have Python 3.7+ installed on your system.

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn plotly scikit-learn scipy
```

Or using requirements.txt:

```bash
pip install -r requirements.txt
```

**requirements.txt:**
```
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
plotly>=5.0.0
scikit-learn>=1.0.0
scipy>=1.7.0
```

## 🚀 Quick Start

### Basic Usage

```python
from furniture_analysis_pipeline import FurnitureAnalysisPipeline

# Initialize the pipeline with your CSV file
analyzer = FurnitureAnalysisPipeline('your_furniture_data.csv')

# Run complete analysis
results = analyzer.run_full_analysis()
```

### Step-by-Step Analysis

```python
# Initialize pipeline
analyzer = FurnitureAnalysisPipeline('furniture_data.csv')

# Individual analysis steps
analyzer.load_and_explore_data()
analyzer.analyze_pricing_strategy()
analyzer.analyze_sales_performance()
analyzer.analyze_product_categories()
analyzer.analyze_tag_text_impact()
analyzer.perform_correlation_analysis()
analyzer.perform_predictive_modeling()
analyzer.perform_customer_segmentation()
analyzer.generate_visualizations()
analyzer.generate_executive_summary()
```

## 📋 Data Requirements

Your CSV file should contain the following columns:

| Column | Type | Description | Required |
|--------|------|-------------|----------|
| `productTitle` | string | Product name/title | ✅ |
| `originalPrice` | numeric | Original price before discount | ✅ |
| `price` | numeric | Current selling price | ✅ |
| `sold` | integer | Number of units sold | ✅ |
| `tagText` | string | Product tags/labels | ⚠️ Optional |

**Sample Data Format:**
```csv
productTitle,originalPrice,price,sold,tagText
"Modern Sofa Set",599.99,449.99,25,"Free shipping, Premium quality"
"Office Chair",129.99,99.99,150,"Free shipping, Ergonomic"
"Dining Table",299.99,299.99,45,"Free shipping"
```

## 📊 Analysis Modules

### 1. Data Exploration
- Dataset overview and statistics
- Data quality assessment
- Missing value analysis
- Duplicate detection

### 2. Pricing Strategy Analysis
- Average and median price analysis
- Discount percentage calculation
- Price tier categorization
- Revenue impact of discounting

### 3. Sales Performance Analysis
- Total units sold and revenue
- Sales performance categorization
- Top-performing products identification
- Revenue analysis by product

### 4. Product Categorization
- Automated furniture type classification
- Category performance metrics
- Market share analysis
- Category-specific insights

### 5. Tag Impact Analysis
- Tag frequency analysis
- Performance comparison (tagged vs untagged)
- Statistical significance testing
- High-impact tag identification

### 6. Correlation Analysis
- Correlation matrix generation
- Strong relationship identification
- Price-sales relationship analysis
- Key insights extraction

### 7. Predictive Modeling
- Linear Regression and Random Forest models
- Sales forecasting capability
- Feature importance analysis
- Model performance evaluation

### 8. Customer Segmentation
- K-means clustering implementation
- Segment characterization
- Strategic recommendations per segment
- Performance metrics by segment

## 📈 Sample Output

The pipeline generates comprehensive analysis including:

```
📈 KEY PERFORMANCE INDICATORS:
  • Total Products Analyzed: 2,000
  • Total Revenue Generated: $2,181,048.07
  • Average Product Price: $156.56
  • Total Units Sold: 46,987
  • Average Discount Rate: 11.5%

🔍 KEY INSIGHTS:
  • Top performing category: Tables (23.8% of revenue)
  • Price neutrality: Price has minimal impact on sales volume
  • Revenue impact of discounts: 40.5% potential revenue lost

💡 STRATEGIC RECOMMENDATIONS:
  1. Prioritize investment in Tables category (highest revenue)
  2. Address high percentage of non-selling products
  3. Implement segment-specific marketing strategies
```

## 📊 Visualizations

The pipeline automatically generates:
- Price and sales distribution histograms
- Correlation heatmaps
- Category performance charts
- Segment analysis plots
- Top product rankings
- Comprehensive dashboard (saved as PNG)

## 🎯 Business Applications

- **E-commerce Optimization**: Identify best-performing products and categories
- **Pricing Strategy**: Optimize discount strategies and price positioning
- **Inventory Management**: Focus on high-revenue generating products
- **Marketing Insights**: Understand tag impact and customer segments
- **Revenue Analysis**: Track performance and identify growth opportunities
- **Competitive Analysis**: Benchmark pricing and performance metrics

## 🔧 Customization

### Adding Custom Categories

```python
# Modify category_mapping in analyze_product_categories method
category_mapping = {
    'Seating': ['chair', 'sofa', 'stool', 'bench'],
    'Tables': ['table', 'desk', 'coffee table'],
    'Storage': ['shelf', 'cabinet', 'dresser'],
    'YourCustomCategory': ['keyword1', 'keyword2']
}
```

### Adjusting Clustering Parameters

```python
# Modify in perform_customer_segmentation method
optimal_k = 5  # Change number of clusters
kmeans = KMeans(n_clusters=optimal_k, random_state=42)
```

## 📝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is unlicensed. 


## 🙏 Acknowledgments

- Built with Python and the amazing data science ecosystem
- Inspired by the need for comprehensive e-commerce analytics
- Special thanks to the open-source community

---
