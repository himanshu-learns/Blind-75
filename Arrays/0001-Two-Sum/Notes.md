## Pattern Recognition 
 - ### Question dikhte hi kiss hint se pattern samajh aaya?
       • Find pair
       • Target sum
       • Need fast lookup
       • Return Indices

## Brute force 
 - ### idea:
       • ek loop se ek element fix Karo ( i = 0 )
       • dusre loop se baaki elements check kro ( j = i + 1 )
       • Agar nums[i] + nums[j] == target equal ho
          • return indices
 - ### Time complexity: O(n²)
 - ### Space complexity: O(1)
 - ### ❌Bad?:
     Baaki elements ke liye har baar elements dubara check karna padega, isse process slow ho jayegi

## Optimized idea: 
   • Array ko sirf ek baar traverse karo 
   • Aur " need = target - current" apply karo
   • Check karo need phele se hai ya nhi 
      • Agar hai to return kardo indices ko current and previous wale elements ke
      • Agar nhi hai toh store kardo hashmap mein 
 - ### Time complexity: O(n)
 - ### Space complexity: O(n)
 - ### ✔️Best?:
    Isse baar-baar array traverse nahi karna padta, hashmap fast lookup ke liye store karta hai

## Algorithm:
   Step 1: Empty HashMap bnao 
   Step 2: Array ko left se right thak traverse karo 
   Step 3: Har element ke liye "need = target-current"
   Step 4: Agar "need" HashMap mein hai toh 
        • return{ hashmap(need), i }  // to know more please go to ( solutioncpp.md ) 
   Step 5: Nahi hai toh
        • nums[i] ko hashmap mein store kar do // go to ( solutioncpp.md ) 
   Step 6: Traverse complete 
        
 
