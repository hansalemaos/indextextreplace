# Replace specific substrings within a given string using index-based replacements

## Tested against Windows / Python 3.11 / Anaconda

## pip install indextextreplace

```python
index_text_replace(string: str, replacements: List[Tuple[int, int, str]]) -> str:
    r"""
    Replace specific substrings within a given string using index-based replacements.

    Args:
        string (str): The input string in which replacements will be made.
        replacements (List[Tuple[int, int, str]]): A list of replacement tuples, where each tuple
            consists of three elements:
            - Start index (int): The starting index of the substring to be replaced (inclusive).
            - End index (int): The ending index of the substring to be replaced (inclusive).
            - Replacement text (str): The text to replace the specified substring with.

    Returns:
        str: A modified string with the specified replacements applied.



    This function replaces substrings within the input `string` according to the provided
    `replacements` list. Each replacement is defined by a start index (inclusive), an end index
    (inclusive), and the replacement text. The replacement is applied to the specified substring
    within the string. The modified string is then returned.

    If the `replacements` list contains overlapping intervals, the behavior of the function is
    defined by the order of the replacements within the list. The last replacement in the list
    for a given index takes precedence.

    Note:
    - Indexing is 0-based.
    - The function does not modify the original input string and returns a new modified string.
    - If the start or end indices of a replacement are out of bounds, they are adjusted to
      the nearest valid index within the string.

    Raises:
        ValueError: If the end index of a replacement is less than the start index."""
		
from indextextreplace import index_text_replace
t = '''Parenthese (altgriechisch παρένθεσις parénthesis, deutsch ‚Einschub')'''
r = [(1, 2, 'XXXX'), (13, 14, 'YYYYY')]
index_text_replace(t, r)
# "PXXXXenthese (aYYYYYgriechisch παρένθεσις parénthesis, deutsch ‚Einschub')"

```

