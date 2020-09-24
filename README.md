# Pascal-s-Triangle
class Solution {
    public List<List<Integer>> generate(int numRows) {
        List<List<Integer>> output= new ArrayList<List<Integer>>();
        for(int line=0;line<numRows;line++){
            List<Integer> currentList = new ArrayList<>();
            for(int i=0;i<=line;i++){
                if(line==i || i==0){
                    currentList.add(1);
                }
                else
                {
                    currentList.add(output.get(line-1).get(i-1)+output.get(line-1).get(i)); 
                }
                
            }
            output.add(currentList);
            
        }
        
        return output;
    }
}
