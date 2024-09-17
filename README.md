# Uncommon-Words-from-Two-Sentences

A sentence is a string of single-space separated words where each word consists only of lowercase letters.
A word is uncommon if it appears exactly once in one of the sentences, and does not appear in the other sentence.
Given two sentences s1 and s2, return a list of all the uncommon words. You may return the answer in any order.

Constraints:
1 <= s1.length, s2.length <= 200
s1 and s2 consist of lowercase English letters and spaces.
s1 and s2 do not have leading or trailing spaces.
All the words in s1 and s2 are separated by a single space.

class Solution(object):
    def uncommonFromSentences(self, s1, s2):
        all_string = s1.split(' ')
        all_string += (s2.split(' '))
        counter = Counter(all_string)

        ans = []
        for s, cnt in counter.items():
            if cnt == 1:
                ans.append(s)
        return ans
