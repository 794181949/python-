### 第一题
Write a program that prints out the decimal value of a Roman numeral.

思路转换罗马数字成阿拉伯数字

    roman = [
    ('M', 1000),
    ('CM', 900),
    ('D', 500),
    ('CD', 400),
    ('C', 100),
    ('XC', 90),
    ('L', 50),
    ('XL', 40),
    ('X', 10),
    ('IX', 9),
    ('V', 5),
    ('IV', 4),
    ('I', 1)
    ]
    numeral = sys.argv[1]
    value = 0 
    i = 0
    while i < len(numeral):
      for x, y in roman:
        if i + len(x) <= len(numeral) and x == numeral[i:i+len(x)]:
          value += v
          i+= len(x)
          break

### 第二题
 prompts the user for a string w of lowercase letters and outputs the longest sequence of consecutive 
 letters that occur in w, but with possibly other letters in between, starting as close as possible to
 the beginning of w.
 思路： 找到最长连续的字母
 
    word = input('letters')
    word = [ord(c) for c in word]
    longest_len = 0
    start = None
    current_start = 0
    while current_start < len(word) - longest_len:
      last_in_sequence = word[current_start]
      for i in range(current_start + 1, len(word)):
        if word[i] - last_in_sequence == 1:
          current_length += 1
          last_in_sequence = word[i]
        if current_length > longest_length:
          longest_length = current_length
          start = current_start
      current_start += 1
    
 ### 第三题
   field_width = max(len(str(p)), len(str(q)))
   left = 0, 1
   rigth = 1, 1
   target = p , q
   mediant = 1, 2
   while mediant != target:
    if mediant[0] * target[1] < target[0] * mediant[1]:
      left_mark = ' '
      right_mart = '*'
    else:
      left_mark = '*'
      right_mark = ' '
    print_mediant(left, left_mark, mediant, right_mark, right, field_width)
    if left_mark = ' ':
      left = mediant
    else:
      right = mediant
    mediant = left[0] + right[0], left[1] +right[1]
  print_mediant(left, ' ', mediant, ' ', right, field_width)
  def print_mediant(left, left_mark, mediant, right_mark, right, w):
    print(f'{left[0]:{w}}/{left[1]:<{w}}'
          f'  {left_mark}  {mediant[0]:{w}}/{mediant[1]:<{w}}  {right_mark}  '
          f'{right[0]:{w}}/{right[1]:<{w}}'
         )

 
