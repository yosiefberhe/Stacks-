# Stacks-

This is stacks in java, it is an assignemnt in my class.

public class A4 {

	
		
		int top;
		int capacity;
		int[] stack;
		
		A4(){
			
			top = -1;
			
			capacity = 10;
			
			stack = new int[capacity];
			
			
		}
		
		public boolean isEmpty() {
			
			return top==-1;
			
		}
		
		public bolean isFull() {
			
			return top==capacity-1;
		}
		
		public int push(int data) {
			
			if(isFull()) {
				
				System.out.println("Stack is full");
			}
			
			return stack[++top]= data;
		}
	
		public int pop() {
			
			if(isEmpty()) {
				System.out.println("stack is empty");
			}
			return stack[top--];
		}
		public int peek() {
			
			return stack[top];
		}
	

	private static void main(String[] args) {
		// TODO Auto-generated method stub
		
		A4 st=new A4();
		
		st.push(34);
		st.push(314);
		st.push(24);
		st.push(14);
		st.push(40);
		System.out.println(st.isEmpty());
		System.out.println(st.isFull());
		System.out.println(st.capacity());
		System.out.println(st.peek());
		System.out.println(st.pop());
	}
	

	}





output

34
314
24
14
40
0
0
0
0
0



//Part B

public class braket_matching{

	public static void main(String a[]) {
	 boolean result=isBalancedExpression("()");
	System.out.println("result: "+result);
}
	private static boolean isBalancedExpression(String exp){

	LIst<Character> stack = new ArrayList<>();
	for(char c:exp.toCharArray()){

	if(c== '(' || c=='['  || c=='}'){
	stack.add(0, c);
} else{
	if(stack.isEmpty()){
	return Boolean.FALSE;
}
	char tmpFromStack = stackget(0);
	if((c==') && tmpFromStack=='(' )
	|| (c ==']' && tmpFromStack =='[')
	|| (c =='}' && tmpFromStack =='{')){
stack.remove(0);
} else{
return Boolean FALSE;
}
}
}

output




Part C

public class A4 {

	public int postfixToEvaluation(String s) {
		Stack<Integer> st = new Stack<Integer>();
		
		int x=0, y=0;
		char ch[] = s.toCharArray();
		for(char c: ch) {
			if(c >='0' && c<= '9') {
				st.push((int) (c-'0'));
			}else {
				y=st.pop();
				x=st.pop();
				
				switch(c) {
				case '+':
					st.push(x+y);
					break;
				case '-':
					st.push(x-y);
					break;
				case '*':
					st.push(x*y);
					break;
				}
			}
			return st.pop();
		}
		
	}
		public static void class StackCal{
			
			public static void main(String[] args) {
				
				StackTmp1 a = new StackImpl();
				String s1 = a.inflixToPostfix("2+3-1");
				System.out.println(a.postfixToEvaluation(s1));
				
				String s2 = a.infixToPostfix("2+3*4");
				System.out.println(a.postfixToEvaluation(s2));
			}
		}
			}


output 

4
14
