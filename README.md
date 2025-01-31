
# GDP Growth Analysis

This project uses the GDP growth dataset provided by the World Bank. The goal is to visualize the GDP growth of different countries over time within a specified year range.

## Function: `plot_country_pib_year_range`

### Description

The `plot_country_pib_year_range` function allows you to visualize the GDP growth of one or more countries over a specified range of years. It generates a plot showing GDP growth over time for each country provided.

### Parameters

- `min_year` (int): The minimum year for the desired year range.
- `max_year` (int): The maximum year for the desired year range.
- `country_list` (list): A list of country names (as strings) whose GDP growth will be analyzed.

### Process

1. **Data Filtering**: The function selects rows corresponding to the countries in the `country_list`.
2. **Data Cleaning**: It removes unnecessary columns such as country codes and indicator codes, and sets the country name as the index.
3. **Data Adjustment**: The data is reorganized so that the year becomes a column, and the year range is adjusted according to the `min_year` and `max_year` parameters.
4. **Visualization**: A line is plotted for each country within the specified year range.

### Example Usage

```python
# List of countries to analyze
countries = ['Argentina', 'Brasil', 'Chile']

# Call the function to see GDP growth between 2000 and 2020
plot_country_pib_year_range(2000, 2020, countries)
```

### Requirements

- `matplotlib`: For generating the plots.
- `pandas`: For handling and cleaning the data.

### Notes

- Ensure that the World Bank dataset is loaded into the `df` DataFrame before calling the function.
- The year range should be between the years available in the dataset.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
