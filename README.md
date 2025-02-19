# React Native FlatList Empty List Bug

This repository demonstrates a common bug in React Native where a FlatList component renders an empty list even though data has been successfully fetched from an API. The issue occurs due to an unexpected data structure or missing key prop. 

## Bug Description

The `DataList` component fetches data from a sample API endpoint.  After successful fetching, instead of displaying the data in the FlatList, an empty list is displayed. The loading state correctly displays while the API is called, but once the data is returned it shows nothing, despite the data being present in the console log. 

## Solution

The solution involves carefully checking the structure of the data received from the API and ensuring that the `keyExtractor` prop of the FlatList is correctly configured to uniquely identify each item in the data array. The solution file (`DataListSolution.js`) demonstrates the corrected implementation.  The bug is in how the data is used to populate the FlatList.