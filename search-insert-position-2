# Given a sorted array and a target value, return the index if the target is found.If not, return the index where it would be if it were inserted in order.
# You may assume no duplicates in the array.
# 
# Example 1 :
# Input : [1, 3, 5, 6], 5
# Output : 2
# 
# Example 2 :
#Input : [1, 3, 5, 6], 2
# Output : 1
# 
# Example 3 :
# Input : [1, 3, 5, 6], 7
# Output : 4
# 
# Example 4 :
# Input : [1, 3, 5, 6], 0
# Output : 0


def search_insert(nums, target)
  @start_index = 0
  @end_index = nums.length - 1
  if target > nums.last
    return nums.length
  elsif target < nums.first
    return 0
  else
    while @start_index <= @end_index
      @mid_index = (@end_index + @start_index) / 2
      if nums[@mid_index] == target
        return @mid_index
      elsif nums[@mid_index] < target
        @start_index += 1
      else
        @end_index -= 1
      end
         
    end
      return nums.bsearch_index{|e| e > target}
  end
end
