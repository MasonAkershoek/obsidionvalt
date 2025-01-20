
---
- # #Selection_Sort
	- This algorithm sorts elements by comparison, it starts by finding the smallest or larges element in the array then swaps it into the first element of the array. then repeats this until the array is sorted.
	- Time Complexity O($n^2$)
	- Advantages
		- Easy to implement
		- low number of memory writes
```
		int n = arr.size();
		
		    for (int i = 0; i < n - 1; ++i) {
		
		        // Assume the current position holds
		        // the minimum element
		        int min_idx = i;
		
		        // Iterate through the unsorted portion
		        // to find the actual minimum
		        for (int j = i + 1; j < n; ++j) {
		            if (arr[j] < arr[min_idx]) {
		
		                // Update min_idx if a smaller
		                // element is found
		                min_idx = j; 
		            }
		        }
		
		        // Move minimum element to its
		        // correct position
		        swap(arr[i], arr[min_idx]);
		    }
```

- # #Bubble_Sort 
	- Simplest sorting algorithem to implement all it dose is continue to iterate through the array swapping the 2 numbers it is acting on until the array is sorted
	- Time Complexity O($n^2$)
```
		int n = arr.size();
	    bool swapped;
	  
	    for (int i = 0; i < n - 1; i++) {
	        swapped = false;
	        for (int j = 0; j < n - i - 1; j++) {
	            if (arr[j] > arr[j + 1]) {
	                swap(arr[j], arr[j + 1]);
	                swapped = true;
	            }
	        }
	      
	        // If no two elements were swapped, then break
	        if (!swapped)
	            break;
		}
```

- # #Insertion_Sort
	- 