# inheritance
package inheritance;
abstract class shape{
        public abstract double calculatearea();
    }
    class circle extends shape{
        private double radius;
        public circle(double radius){
            this.radius=radius;
        }
        public double calculatearea(){
            return Math.PI*radius*radius;
        }
    }
    class rectangle extends shape{
        double length,width;
        public rectangle(double length,double width){
            this.length=length;
            this.width=width;
        }
        public double calculatearea(){
            return length*width;
        }
    }
    class square extends shape{
        double side;
        public square(double side){
            this.side=side;
        }
        public double calculatearea(){
            return side*side;
        }
    } 
    class triangle extends shape{
        double base,height;
        public triangle(double base,double height){
            this.base=base;
            this.height=height;
        }
        public double calculatearea(){
            return base*height;
        }
    }



public class Inheritance {
    public static void main(String[] args) {
        shape circle=new circle(5);
        shape rectangle=new rectangle(5,3);
        shape square=new square(5);
        shape triangle=new triangle(4,5);
        
        System.out.println("circle area:"+circle.calculatearea());
        System.out.println("rectangle area:"+rectangle.calculatearea());
        System.out.println("square area:"+square.calculatearea());
        System.out.println("triangle area:"+triangle.calculatearea());
        
        
    }
}

        
run:
circle area:78.53981633974483
rectangle area:15.0
square area:25.0
triangle area:20.0

