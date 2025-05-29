Created on: 28-05-2025 23:20
Status: #idea
Tags: #OS
# Compare & Swap
is a hardware instruction that is atomically.
- set to `new_value` only if the expression `*value=expected`
- Regardless, it always returns the original value of `value`
```
int compare_and_swap(int *value, int expected, int new_value) { 
	int temp = *value;
	if (*value == expected)
		*value = new_value;
	return temp;
}
```

To check how Mutual exxlusion happens check -->[[Mutual exclusion with CAS#Mutual Exclusion with CAS]]



-----------------
# References