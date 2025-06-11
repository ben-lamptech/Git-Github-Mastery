# -------------------------------
# **Lambda Function Template
# -------------------------------
## format: lambda x: condition
### - x = parameter (can be named anything: x, item, pair, etc.)
### - condition = expression returning True/False

## Example:
```python
lambda x: x[1] in valid_formats
```
### - x = each tuple from zipped list
### - x[1] = format (2nd item in tuple)
### - returns True if format is in valid_formats

# -------------------------------
# zip() Function
# -------------------------------
## zip(list1, list2)
### - Pairs elements: [(list1[0], list2[0]), (list1[1], list2[1]), ...]
### - Stops at shortest list (truncates silently if lengths differ)

## Example:
```python
zip(doc_names, doc_formats)
```


# -------------------------------
# filter() Function
# -------------------------------
## filter(function, iterable)
### - function = returns True/False
### - iterable = data to filter
### - Returns an iterator of items where function(item) is True

## Example:
```python 
filter(lambda x: x[1] in valid_formats, zip(doc_names, doc_formats))
```

## Convert to list:
```python
list(filter(lambda x: x[1] in valid_formats, zip(doc_names, doc_formats)))
```

# -------------------------------
# Full Function Example
# -------------------------------
## valid_formats = ["docx", "pdf", "txt", "pptx", "ppt", "md"]
```python
def pair_document_with_format(doc_names, doc_formats):
    return list(filter(lambda x: x[1] in valid_formats, zip(doc_names, doc_formats)))
```  
# -------------------------------
# Alternative with Named Function
# -------------------------------
```python
def is_valid_format(pair):
    return pair[1] in valid_formats

def pair_document_with_format_alt(doc_names, doc_formats):
    return list(filter(is_valid_format, zip(doc_names, doc_formats)))
```
# -------------------------------
# Alternative using List Comprehension
# -------------------------------
```python
def pair_document_with_format_lc(doc_names, doc_formats):
    return [(name, fmt) for name, fmt in zip(doc_names, doc_formats) if fmt in valid_formats]
```
