# &lt;highcharts-chart&gt;

> Web Component wrapper to the [Highcharts Graphing Library](http://www.highcharts.com/), to create a multitude of graphs (spline, pie, and more) using [Polymer 1.0](http://www.polymer-project.org/1.0/).

## Demo

[Check it live!](http://avdaredevil.github.io/highcharts-chart)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install highcharts-chart --save
```

Or [download as ZIP](https://github.com/avdaredevil/highcharts-chart/archive/master.zip).

## Usage

1. Import Web Components' polyfill, on older browsers:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents-lite.min.js"></script>
    ```

2. Import Custom Element:

    ```html
    <link rel="import" href="bower_components/highcharts-chart/highcharts-chart.html">
    ```

3. Start using it!

    ```html
    <highcharts-chart type="spline"></highcharts-chart>
    <highcharts-chart type="pie"></highcharts-chart>
    ```

## &lt;highcharts-chart&gt;

Provides you a simple interface to interact with the HighCharts API, with Data Binding.
The charting is also responsive.

### Options

Attribute  | Options     | Default              | Description
---        | ---         | ---                  | ---
`type`     | `spline`,`pie` | `false`           | Pick type of chart
`title`    | *string*    | `Highcharts Chart`   | Title of Chart
`subtitle` | *string*    | `""`                 | Subtitle of Chart
`showAxes` | *array*     | `['bottom','left']`  | Pick the axes to show.
`xAxis`    | *object*    | `{}` OR *`Time based`* | Specifies the configuration for the X-Axis.
`yLabel`   | *string*    | `Y-Axis`             | Label for Y-Axis
`label`    | *string*    | `Label`*`[for non numeric]`* | Alias for y-label
`data`     | *array*     | `[]` | Data for chart
`loading`  | *boolean*     | `false` | Toggle loading overlay on chart
`loadingMessage` | *string* | `Loading...` | Loading Text Display
`selected` | *boolean*     | `false` | Is any element selected on graph
`selectedPoints` | *array* | `[]` | Which elements are selected
`vsTime`   | *boolean*     | `false` | Set all options appropriate for a time chart
`legend`   | *boolean*   | `false`              | Display the legend
`credits`  | *boolean*     | `false` | Wish to thank/credit HighCharts?

### Methods

Method       | Parameters           | Returns            | Description
---          | ---                  | ---                | ---
`setData()`  | `Data Array [e,e,e]` | Nothing.           | Replaces graph data with this
`addData()`  | `Data` [*x*,*y*]     | Nothing.           | Appends to data [*efficient*]
`pushData()` | `Data` [*x*,*y*]     | Nothing.           | Shifts and adds to data [*efficient*]

### Events

Event      | Description
---        | ---
`NA`       | NA

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## License

[MIT License](http://avdaredevil.mit-license.org/) © Apoorv Verma