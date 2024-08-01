# Number-of-senior-citizens
class Solution {
    public int countSeniors(String[] details) {
        int count = 0;
        
        for (String detail : details) {
            // Extract the age part of the string
            String ageStr = detail.substring(11, 13);
            int age = Integer.parseInt(ageStr);
            
            // Check if the age is strictly greater than 60
            if (age > 60) {
                count++;
            }
        }
        
        return count;
    }
    
    public static void main(String[] args) {
        // Sample input
        String[] details = {
            "1234567890M6101",
            "0987654321F5802",
            "1122334455M7012",
            "6677889900F7503"
        };
        
        // Create an instance of Solution
        Solution solution = new Solution();
        
        // Call the function to get the number of passengers older than 60
        int count = solution.countSeniors(details);
        
        // Print the result
        System.out.println(count); // Output should be 2 for this example
    }
}
