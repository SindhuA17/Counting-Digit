# Counting-Digit

Logic and algorithm :

Algorithm Explanation:

The algorithm uses a loop to iterate through each place value (ones, tens, hundreds, etc.) in the range from 0 to n. The variable count accumulates the total count of digit 1 in this range.

Details of the Algorithm:

Initialize count to 0, factor to 1, and i to 1.

Start a loop that continues until i becomes greater than n.

Inside the loop, calculate divider as i * 10. This divider represents the next higher place value.

Update count using the following formula:
count += (n // divider) * i + min(max(n % divider - i + 1, 0), i)
(i) (n // divider) * => This part counts the occurrences of digit 1 at the current place value for the full cycles (e.g., in the tens, hundreds, etc. places).
(ii) min(max(n % divider - i + 1, 0), i) => This part handles the remaining digits at the current place value after the full cycles. It ensures that we don't count more than the actual remaining digits.

Multiply i by 10 to move on to the next lower place value.

Repeat the loop until the entire range is covered.

Return the final count.
