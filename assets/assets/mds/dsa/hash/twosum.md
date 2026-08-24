🧩 Two Sum: The Power of a Hash Map

The Two Sum problem is arguably the most famous coding interview question in the world. The premise is simple: Given an array of numbers and a target sum, find the indices of the two numbers that add up exactly to that target.

For example: Array = [2, 7, 11, 15], Target = 9. (The answer is Index 0 and Index 1, because 2 + 7 = 9).

🐢 The Brute Force Approach (The Slow Way)

The most obvious way to solve this is to use a nested for loop. You take the first number (2), and then scan every other number in the array to see if it adds up to 9. Then you move to the second number (7) and scan everything else again.

This means you are checking every single possible combination. If your array has 100,000 items, that is 10 billion comparisons. This approach takes $O(N^2)$ time, which is terrible for performance.

⚡ The Hash Map Solution (The Clever Way)

We can solve this in a single pass—$O(N)$ time—by giving our algorithm a "photographic memory" using a Hash Map.

Instead of looking forward and checking every combination, we only look at the number in front of us, figure out exactly what puzzle piece we are missing, and ask the Hash Map if we've seen it already.

The Algorithm Step-by-Step

Imagine our target is 9, and we are scanning the array [2, 7, 11, 15]. We start with an empty Hash Map.

Rule: We store Key: Number ➔ Value: Index in the Map.

Scan Index 0 (Value is 2):

The Math: If I have 2, and my target is 9, what do I need? 9 - 2 = 7. My Complement is 7.

The Check: Hey Hash Map, do you have a 7?

The Result: The map is empty. No.

The Action: I will store myself in the map so others can find me later. Map now holds: {2 : 0}.

Scan Index 1 (Value is 7):

The Math: If I have 7, what do I need to hit 9? 9 - 7 = 2. My Complement is 2.

The Check: Hey Hash Map, do you have a 2 in your memory?

The Result: Yes! It was stored at Index 0.

The Action: Match Found! We immediately return our current index (1) and the map's index (0).

⚠️ Crucial Pitfalls to Avoid

Storing before Checking: You MUST check the Hash Map for the complement before you save your current number to the map. If your target is 8, and you scan the number 4, if you store the 4 first, the map will immediately say "I found a 4!" and use the exact same number twice.

Storing the wrong Value: Beginners often map the Array Index as the Key and the Number as the Value. This defeats the purpose! A Hash Map can only instantly search its Keys. We need to ask "Have I seen this Number?", so the Number must be the Key.

⏱️ Complexity

Time Complexity: $O(N)$ — We only scan the array exactly one time. Hash Map lookups (map.containsKey()) take instant $O(1)$ time, making the overall algorithm incredibly fast.

Space Complexity: $O(N)$ — We trade time for space. In the worst-case scenario (the matching pair is at the very end of the array, or doesn't exist at all), we end up storing almost every single number inside the Hash Map, requiring extra memory.