In [40]: obj3
Out[40]: 
Ohio      35000
Texas     71000
Oregon    16000
Utah       5000
dtype: int64

In [41]: obj4
Out[41]: 
California        NaN
Ohio          35000.0
Oregon        16000.0
Texas         71000.0
dtype: float64

In [42]: obj3 + obj4
Out[42]: 
California         NaN
Ohio           70000.0
Oregon         32000.0
Texas         142000.0
Utah               NaN
dtype: float64

当你对两个 Pandas Series 进行加法运算时，Pandas 会对齐两个 Series 的索引，然后对相应位置的值进行运算。如果某个索引在其中一个 Series 中不存在（即缺失值），结果中的该位置将会是 NaN。

Type	                                      Notes
2D ndarray	                                  A matrix of data, passing optional row and column labels
Dictionary of arrays, lists, or tuples	      Each sequence becomes a column in the DataFrame; all sequences must be the same length
NumPy structured/record array	              Treated as the “dictionary of arrays” case
Dictionary of Series	                      Each value becomes a column; indexes from each Series are unioned together to form the result’s row index if no explicit index is passed
Dictionary of dictionaries	                  Each inner dictionary becomes a column; keys are unioned to form the row index as in the “dictionary of Series” case
List of dictionaries or Series	              Each item becomes a row in the DataFrame; unions of dictionary keys or Series indexes become the DataFrame’s column labels
List of lists or tuples	                      Treated as the “2D ndarray” case
Another DataFrame	                          The DataFrame’s indexes are used unless different ones are passed
NumPy MaskedArray	                          Like the “2D ndarray” case except masked values are missing in the DataFrame result




Index Object:
Index objects are immutable