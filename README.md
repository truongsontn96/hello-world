## Extend Queries Plugin for Emerald:
Extend Queries plugin is built as a data source plugin and can be used in conjunction with other data source to show computed metrics like Moving Average, Time Shift.
  
## Installation
Need to clone this repo into your Emerald plugins directory (default /var/lib/Emerald/plugins if your installing Emerald with package).
Restart Emerald-server and the plugin should be automatically detected and used.

```
git clone git@github.com:GoshPosh/Emerald-extend-query.git
sudo service Emerald-server restart
```  

Create a new datasource with a name and select `type` as `ExtendQueries`
![Screenshot](https://raw.githubusercontent.com/GoshPosh/Emerald-extend-query/master/img/DataSourceConfig.png?raw=true "DataSource")

## Usage
* Set the Graph's data source to `ExtendQueries`
* Add query of your data source (add a few more)
* Add query with `ExtendQueries` as data source
* Reference other columns as `A` or `B` depending on what is shown 

## Examples
#### Arithmetic
Lets you perform arithmetic operations on one or more existing queries.
![Screenshot](https://raw.githubusercontent.com/GoshPosh/Emerald-extend-query/master/img/arithmetic-ex1.png?raw=true "Arithmetic Example 1 - Metric * 2")
![Screenshot](https://raw.githubusercontent.com/GoshPosh/Emerald-extend-query/master/img/arithmetic-ex2.png?raw=true "Arithmetic Example 2 - Metric A + Metric B")

#### Moving Average
![Screenshot](https://raw.githubusercontent.com/GoshPosh/Emerald-extend-query/master/img/moving_average-ex1.png?raw=true "Moving Average Example 1 - 7 period moving average of Metric A ")

#### Time Shift
![Screenshot](https://raw.githubusercontent.com/GoshPosh/Emerald-extend-query/master/img/time_shift-ex1.png?raw=true "Time Shift Example 1 - 1 period timeshift of Metric A ")


## Compatibility
Emerald Extend Queries plugin 0.0.1 and above are supported for Emerald: 4.x.x


## Supports Nesting 
* Moving average of moving average
* Moving average of time shift
* Time shift of Moving average 
* Time shift of Time Shift

## Known issue
* Moving average on arithmetic is not supported
* TimeShift on arithmetic is not supported


## Status
Lot of features might still not be implemented. Your contributions are welcome.

