package start;

import java.util.Arrays;
import java.util.HashMap;
import java.util.Map;
import java.util.Set;

public class HashMap3 {
	
					public static void main(String[] args)
					{
						
							String name = "This is a Name";
							char [] y =name.toCharArray();
							System.out.println(Arrays.toString(y));
							int size = y.length;
							
							Map<Character,Integer>map =new HashMap<>();
							int i=0;
							while(i!=size)
							{
								if(map.containsKey(y[i])==false)
								{
									map.put(y[i], 1);
								}
								else
								{
									int oldval = map.get(y[i]);
									int newval = oldval +1;
									map.put(y[i], newval);
								}
								i++;
							}
//							Set<Map.Entry<Character, Integer>>hmap=map.entrySet();
//			   				for(Map.Entry<Character,Integer>data1 : hmap)
							
							
								Set<Map.Entry<Character, Integer>>lhmap=map.entrySet();	
								for(Map.Entry<Character, Integer>data :lhmap)
								{
									System.out.println(data.getKey());
									System.out.println(data.getValue());
								}
							
					}

}


/********************************Minmax****************************************/

package start;

public class MinMax {

			 void  min(int a[])
			{
				int min = a[0];
				for(int i=1;i<a.length;i++)
				{
					if(min>a[i])
					{
						min=a[i];
					}
				}
				System.out.println(min);
			}
			
			 void max(int b[])
			{
				int max = b[0];
				for(int j=1;j<b.length;j++)
				{
					if(max<b[j])
					{
						max=b[j];
					}
				}
				System.out.println(max);
				
			}
			public static void main(String[] args) {
				int [] a = {39,29,40,8,48};
				MinMax mm = new MinMax();
			    mm.max(a);
			    mm.min(a);
          
          
          
          /*********************Comparator and Conparable**********************************/
          
          package start;

import java.util.ArrayList;
import java.util.Collections;
import java.util.Comparator;

public class Comparable_and_Comparator {
	public static void main(String[] args) {
ArrayList <Integer>al = new ArrayList<Integer>();
al.add(750);
al.add(875);
al.add(465);
al.add(555);
al.add(695);
System.out.println(al);
Collections.sort(al);
System.out.println(al);
Comp c = new Comp();
Collections.sort(al,c);
System.out.println(al);
	}
}
class Comp implements Comparator<Integer>
{

	@Override
	public int compare(Integer o1 ,Integer o2 ) {
		if(o1%100>o2%100)
		{
			return 1;
		}
		return -1;
	}
	
}

