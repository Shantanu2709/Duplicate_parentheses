# Duplicate_parentheses
Solve this problem in Linear time complexity O(n)...
import java.util.*;
class HelloWorld {
    static boolean isDuplicate(String str)
    {
      Stack<Character> s = new Stack<>();
      for(int i=0; i<str.length(); i++)
      {
          char ch = str.charAt(i);
          if(ch=='(' || ch=='a' ||ch=='b' ||ch=='+')
          {
              s.push(ch);
          }
          if(ch==')')
          {
              int count=0;
              while(s.peek()!='(')
              {
                  s.pop();
                  count++;
              }
              if(count<1)
              {
                  return true;
              }
              
          }
      }
      return false;

    }
