# My Financial Expenses Chart

This is a simple HTML file that uses Google Charts to display a pie chart of financial expenses. The chart is divided into different categories such as Housing, Transportation, Food, Utilities, and Entertainment.

## How to Use

1. Open the `chart-for-notion.html` file in your web browser.
2. The pie chart will automatically load and display the financial expenses.

## Code Overview

The HTML file includes a script that uses Google Charts to draw a pie chart.

```html
<script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
<script type="text/javascript">
  google.charts.load('current', {'packages':['corechart']});
  google.charts.setOnLoadCallback(drawChart);

  function drawChart() {
    var data = google.visualization.arrayToDataTable([
      ['Category', 'Amount'],
      ['Housing', 1000],
      ['Transportation', 600],
      ['Food', 300],
      ['Utilities', 400],
      ['Entertainment', 200]
    ]);

    var options = {
      title: 'My Financial Expenses',
      pieHole: 0.4,
    };

    var chart = new google.visualization.PieChart(document.getElementById('googleChart'));
    chart.draw(data, options);
  }
</script>