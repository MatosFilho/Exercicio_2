# Exercicio_2
Aprendendo as vantagens do uso de subclasses
class Shape {
	private String name;
	Shape(String aName){ name = aName; }
	public String getName(){ return name; }
	public float calculateArea(){ return 0.0f; }
	
	static class Circle extends Shape{
		private int radius;
		Circle(String aName){
			super(aName);
			radius = 3;
		}
		
		public float calculateArea(){
			float area;
			area = (float) (3.14*radius*radius);
			return area;
		}
	}
	
	static class Square extends Shape{
		private int side;
		Square(String aName){
			super(aName);
			side = 3;
		}
		
		public float calculateArea(){
			int area;
			area = side*side;
			return area;
		}
	}
	
	static class Triangle extends Shape{
		private int base;
		private int height;
		Triangle (String aName){
			super (aName);
			base = 3;
			height = 4;
		}
		
		public float calculateArea(){
			int area;
			area = base*height/2;
			return area;
		}
	}
	
	
	public static void main(String argv[]) {
		// TODO Auto-generated method stub
		Square s = new Square("Square S");
		Circle c = new Circle("Circle C");
		Triangle t = new Triangle("Triangle T");
		Shape shapeArray[] = {c,s,t};
		for(int i = 0; i < shapeArray.length; i++){
			System.out.println("The area of " + shapeArray[i].getName()
					+ " is " + shapeArray[i].calculateArea() + " sq. cm.\n");
		}
	}
}
