---
title: "[데이터 시각화] Quick Chart를 활용하여 차트 만들기📊"
excerpt: "Open API quickchart.io를 활용하여 차트를 만들어 데이터를 시각화 해보자"
categories: Python
tag: [Python]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

간단하게 차트를 생성할 수 있는 Open API인 [quickchart.io](https://quickchart.io){:target="_blank"}에 대한 차트 생성 실습
- [Gallery](https://quickchart.io/gallery){:target="_blank"}에서 예시 차트들을 확인할 수 있습니다.

## QuickChart Editor
[QuickChart Editor](https://quickchart.io/sandbox#%7B%22chart%22%3A%22%7B%5Cr%5Cn%20%20type%3A%20'doughnut'%5B%E2%80%A6%5Dion%22%3A%222%22%2C%22backgroundColor%22%3A%22%23fff%22%7D){:target="_blank"}를 사용하여 차트를 직접 생성할 수 있습니다.

## Quickchart Python
[quickchart-python](https://github.com/typpo/quickchart-python){:target="_blank"}를 사용하여 파이썬에서 실행할 수 있습니다.

### quickchart.io 설치 방법
```py
pip install quickchart.io
```

### 예시 코드
```py
from quickchart import QuickChart

qc = QuickChart()
qc.width = 500
qc.height = 300

# Config can be set as a string or as a nested dict
qc.config = """{
  type: 'bar',
  data: {
    labels: ['Q1', 'Q2', 'Q3', 'Q4'],
    datasets: [{
      label: 'Users',
      data: [50, 60, 70, 180]
    }]
  }
}"""

# You can get the chart URL...
print(qc.get_url())

# Get the image as a variable...
image = qc.get_image()

# Or write the chart to a file
qc.to_file('mychart.png')
```

### 결과
- Bar 그래프
  ![quickchart](https://quickchart.io/chart?c=%7B%0D%0A%20%20type%3A%20%27bar%27%2C%0D%0A%20%20data%3A%20%7B%0D%0A%20%20%20%20labels%3A%20%5B%27Q1%27%2C%20%27Q2%27%2C%20%27Q3%27%2C%20%27Q4%27%5D%2C%0D%0A%20%20%20%20datasets%3A%20%5B%7B%0D%0A%20%20%20%20%20%20label%3A%20%27Users%27%2C%0D%0A%20%20%20%20%20%20data%3A%20%5B50%2C%2060%2C%2070%2C%20180%5D%0D%0A%20%20%20%20%7D%5D%0D%0A%20%20%7D%0D%0A%7D%0D%0A)

## 실습 : 한국 코로나19 감염 추이
Python 스크립트에서 Quick Chart 모듈을 사용하지 않고 json 파라미터 형식으로 전달했습니다.

### 코드
```py
chart = {
    "type": "bar",
    "data": {
        "labels": self.chart_labels,
        "datasets": [
            {
                "type": "line",
                "label": text.get('plot_data_one'),
                "borderColor": "rgb(255, 99, 132)",
                "backgroundColor": "rgba(255, 99, 132, 0.5)",
                "fill": "false",
                "data": self.chart_data
            }
        ]
    },
    "options": {
        "title": {
            "display": "true",
            "text": text.get('plot_title'),
        },
        "scales": {
            "xAxes": [
                { "scaleLabel": { "display": "true", "labelString": text.get('plot_xlabel') } }
            ],
            "yAxes": [
                {
                    "ticks": { "beginAtZero": "true" },
                    "scaleLabel": { "display": "true", "labelString": text.get('plot_ylabel') },
                }
            ]
        }
    }
}

chartUrl = 'https://quickchart.io/chart?bkg=%23ffffff&c='
chartUrl += parse.urlencode({'data': json.dumps(chart)})
```

### 결과
- Line 그래프
  ![quickchart](https://quickchart.io/chart?bkg=%23ffffff&c=data=%7B%22type%22%3A+%22bar%22%2C+%22data%22%3A+%7B%22labels%22%3A+%5B%222022-12-18%22%2C+%222022-12-19%22%2C+%222022-12-20%22%2C+%222022-12-21%22%2C+%222022-12-22%22%2C+%222022-12-23%22%2C+%222022-12-24%22%2C+%222022-12-25%22%2C+%222022-12-26%22%2C+%222022-12-27%22%2C+%222022-12-28%22%2C+%222022-12-29%22%2C+%222022-12-30%22%5D%2C+%22datasets%22%3A+%5B%7B%22type%22%3A+%22line%22%2C+%22label%22%3A+%22%5Cud655%5Cuc9c4%22%2C+%22borderColor%22%3A+%22rgb%28255%2C+99%2C+132%29%22%2C+%22backgroundColor%22%3A+%22rgba%28255%2C+99%2C+132%2C+0.5%29%22%2C+%22fill%22%3A+%22false%22%2C+%22data%22%3A+%5B%2258862%22%2C+%2226622%22%2C+%2287559%22%2C+%2288172%22%2C+%2275744%22%2C+%2268168%22%2C+%2266211%22%2C+%2258448%22%2C+%2225545%22%2C+%2287596%22%2C+%2287517%22%2C+%2271427%22%2C+%2265207%22%5D%7D%5D%7D%2C+%22options%22%3A+%7B%22title%22%3A+%7B%22display%22%3A+%22true%22%2C+%22text%22%3A+%22%5Cud55c%5Cuad6d%5Cuc758+%5Cucf54%5Cub85c%5Cub09819+%5Cuac10%5Cuc5fc+%5Cucd94%5Cuc774%22%7D%2C+%22scales%22%3A+%7B%22xAxes%22%3A+%5B%7B%22scaleLabel%22%3A+%7B%22display%22%3A+%22true%22%2C+%22labelString%22%3A+%22%5Cuc77c%5Cuc790%22%7D%7D%5D%2C+%22yAxes%22%3A+%5B%7B%22ticks%22%3A+%7B%22beginAtZero%22%3A+%22true%22%7D%2C+%22scaleLabel%22%3A+%7B%22display%22%3A+%22true%22%2C+%22labelString%22%3A+%22%5Cuac74%5Cuc218%22%7D%7D%5D%7D%7D%7D)


## 실습 : 이중 파이/도넛 그래프
### 코드
```json
{
  type: 'doughnut',
  data: {
    datasets: [
      {
        data: [27, 26, 85, 2],
        backgroundColor: [
          'rgb(255, 99, 132)',
          'rgb(255, 159, 64)',
          'rgb(255, 205, 86)',
          'rgb(75, 192, 192)',
          'rgb(54, 162, 235)',
        ],
      },
      {
        data: [27, 0, 26, 0, 67, 18, 0, 2],
        backgroundColor: [
          'rgb(255, 99, 132)',
          'rgb(255, 255, 255)',
          'rgb(255, 159, 64)',
          'rgb(255, 255, 255)',
          'rgb(255, 205, 86)',
          'rgb(255, 255, 255)',
          'rgb(75, 192, 192)',
          'rgb(255, 255, 255)',
          'rgb(54, 162, 235)',
          'rgb(255, 255, 255)',
        ],
      },
    ],
    labels: ['Chocolate', 'Mont Blanc', 'Cheese Cake', 'Macaron'],
  },
  options: {
    title: {
      display: true,
      text: 'Donut Chart（2022.12.30）',
    },
    plugins: {
      datalabels: {
        display: true,
        formatter: (data, ctx) => {
          if (ctx.datasetIndex == 1 && (ctx.dataIndex % 2 == 1 || ctx.dataIndex == 6)) {
            return null;
          } else {
            return data + '명';
          }
        },
        color: '#444',
        font: {
          size: 12,
        },
      },
      doughnutlabel: {
        labels: [
          {
            text: '전체 합계',
            font: {
              size: 12,
            }
          },
          {
            text: '140명',
            font: {
              size: 15,
              weight: 'bold'
            }
          },
          {
            text: '',
          },
          {
            text: '안쪽 파이 합계',
            font: {
              size: 12,
            }
          },
          {
            text: '120명',
            font: {
              size: 15,
              weight: 'bold'
            }
          },
        ]
      }
    }
  }
}
```

### 코드 경량화(Minify)
[https://www.minifier.org/](https://www.minifier.org/){:target="_blank"}

### 차트 배경 색 설정
![images](/images/2022-12-30-quick-chart/quick-chart.png)

### 결과
- Double doughnut 그래프
  ![chart](https://quickchart.io/chart?bkg=%23ffffff&c=%7Btype%3A%27doughnut%27%2Cdata%3A%7Bdatasets%3A%5B%7Bdata%3A%5B27%2C26%2C85%2C2%5D%2CbackgroundColor%3A%5B%27rgb(255%2C%2099%2C%20132)%27%2C%27rgb(255%2C%20159%2C%2064)%27%2C%27rgb(255%2C%20205%2C%2086)%27%2C%27rgb(75%2C%20192%2C%20192)%27%2C%27rgb(54%2C%20162%2C%20235)%27%2C%5D%2C%7D%2C%7Bdata%3A%5B27%2C0%2C26%2C0%2C67%2C18%2C0%2C2%5D%2CbackgroundColor%3A%5B%27rgb(255%2C%2099%2C%20132)%27%2C%27rgb(255%2C%20255%2C%20255)%27%2C%27rgb(255%2C%20159%2C%2064)%27%2C%27rgb(255%2C%20255%2C%20255)%27%2C%27rgb(255%2C%20205%2C%2086)%27%2C%27rgb(255%2C%20255%2C%20255)%27%2C%27rgb(75%2C%20192%2C%20192)%27%2C%27rgb(255%2C%20255%2C%20255)%27%2C%27rgb(54%2C%20162%2C%20235)%27%2C%27rgb(255%2C%20255%2C%20255)%27%2C%5D%2C%7D%2C%5D%2Clabels%3A%5B%27Chocolate%27%2C%27Mont%20Blanc%27%2C%27Cheese%20Cake%27%2C%27Macaron%27%5D%2C%7D%2Coptions%3A%7Btitle%3A%7Bdisplay%3A!0%2Ctext%3A%27Donut%20Chart%EF%BC%882022.12.30%EF%BC%89%27%2C%7D%2Cplugins%3A%7Bdatalabels%3A%7Bdisplay%3A!0%2Cformatter%3A(data%2Cctx)%3D%3E%7Bif(ctx.datasetIndex%3D%3D1%26%26(ctx.dataIndex%252%3D%3D1%7C%7Cctx.dataIndex%3D%3D6))%7Breturn%20null%7Delse%7Breturn%20data%2B%27%EB%AA%85%27%7D%7D%2Ccolor%3A%27%23444%27%2Cfont%3A%7Bsize%3A12%2C%7D%2C%7D%2Cdoughnutlabel%3A%7Blabels%3A%5B%7Btext%3A%27%EC%A0%84%EC%B2%B4%20%ED%95%A9%EA%B3%84%27%2Cfont%3A%7Bsize%3A12%2C%7D%7D%2C%7Btext%3A%27140%EB%AA%85%27%2Cfont%3A%7Bsize%3A15%2Cweight%3A%27bold%27%7D%7D%2C%7Btext%3A%27%27%2C%7D%2C%7Btext%3A%27%EC%95%88%EC%AA%BD%20%ED%8C%8C%EC%9D%B4%20%ED%95%A9%EA%B3%84%27%2Cfont%3A%7Bsize%3A12%2C%7D%7D%2C%7Btext%3A%27120%EB%AA%85%27%2Cfont%3A%7Bsize%3A15%2Cweight%3A%27bold%27%7D%7D%2C%5D%7D%7D%7D%7D)

## Reference
- github
[https://github.com/typpo/quickchart](https://github.com/typpo/quickchart){:target="_blank"}