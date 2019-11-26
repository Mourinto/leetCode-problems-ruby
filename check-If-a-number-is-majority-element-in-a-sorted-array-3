# Given an array nums sorted in non - decreasing order, and a number target, return True if and only if target is a majority element.

# A majority element is an element that appears more than N / 2 times in an array of length N.
 
# Example 1 :
 
# Input : nums = [2, 4, 5, 5, 5, 5, 5, 6, 6], target = 5
# Output : true
# Explanation :
# The value 5 appears 5 times and the length of the array is 9.
# Thus, 5 is a majority element because 5 > 9 / 2 is true.
 
# Example 2 :
 
# Input : nums = [10, 100, 101, 101], target = 101
# Output : false
# Explanation :
#     The value 101 appears 2 times and the length of the array is 4.
#     Thus, 101 is not a majority element because 2 > 4 / 2 is false.
 
# Note :
 
#     1 <= nums.length <= 1000
#     1 <= nums[i] <= 10 ^ 9
#     1 <= target <= 10 ^ 9

def is_majority_element(nums, target)
  last_index = get_target_index(nums, target, true)
  return false if last_index == -1
  first_index = get_target_index(nums, target, false)
  (last_index - first_index + 1) > (nums.length / 2) 
end

def get_target_index(nums, target, last_index)
  @start = 0
  @end = nums.length - 1
  @index = -1
  while @start <= @end
    @mid = @start + (@end - @start) / 2
    if nums[@mid] == target
      @index = @mid
      if last_index
        @start = @mid + 1
      else
        @end = @mid - 1
      end
    elsif nums[@mid] > target
      @end = @mid - 1
    else
      @start = @mid + 1
    end
  end
   @index
end
