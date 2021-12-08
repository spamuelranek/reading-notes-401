# To comprehend a list you must
# have the list comprehend you
# thus List Comprehensions

# [List Comprehensions](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)
```python
the_list_of_my_eliminated_enemies = [eliminate for enemy in enemies]
```
- first we will `eliminate`
- second we will carry out the fist step on `enemy`
- thired we get these `enemy` from the list `enemies`
- finally the `the_list_of_my_eliminate_enemies` stores the list that has had the expression(`eliminate`) done to each item(`enemy`) in the list(`enemies`)

- Create a list of values using a range
```python
befouled_values = [all for all in range(10)]
print(befouled_vales) ==> [0,1,2,3,4,5,6,7,8,9]
```

- Filters on list comprehensions
```python
gets_to_live = [eliminate for person in good_and_bad_person_list if person.good_or_bad = "good"]
```