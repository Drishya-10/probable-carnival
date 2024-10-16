print(2363025)
class Shape:
    def __init__(self,area,perimeter):
        self.area=area
        self.perimeter=perimeter
class Circle(Shape):
    def __init__(self,radius,area,perimeter):
        super(Circle,self).__init__(area,perimeter)
        self.radius=radius
    def calculate_area(self):
        a=3.14*self.radius*self.radius
        print(f"area={a}")
    def calculate_cir(self):
        b=2*3.14*self.radius
        print(f"circumfence={b}")
class Rect(Shape):
    def __init__(self,length,breadth,area,perimeter):
        super(Rect,self).__init__(area,perimeter)
        self.length=length
        self.breadth=breadth
    def calculate_area(self):
        c=self.length*self.breadth
        print(f"area={c}")
    def calculate_perimeter(self):
        d=2*(self.length+self.breadth)
        print(f"perimeter={d}")
def main():
    while True:
        print("enter choice")
        print("1.Circle")
        print("2.Rectangle")
        print("3.exit")
        choice=int(input("enter your choice"))
        if choice==1:
            radius=int(input("enter radius"))
            circle=Circle(radius,0,0)
            circle.calculate_area()
            circle.calculate_cir()
        elif choice==2:
            length=int(input("enter length"))
            breadth=int(input("enter breadth"))
            rect=Rect(length,breadth,0,0)
            rect.calculate_area()
            rect.calculate_perimeter()
        elif choice==3:
            print("Exiting..")
            break
        else:
            print("invalid choice")
if __name__ =="__main__":
    main()
