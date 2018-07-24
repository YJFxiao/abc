# abc
abc
object tempt {
  def main(args:Array[String])={
    var temp=List(29,38,27,33,36,39,35)
    println("一周的气温为："+temp)
    for(i<-Range(0,7)){
      if(i==2)
        print("周三的温度为："+temp(i))
    }
  }
  1.to(10).map(j=>j*10).foreach(j=>println(j))

  for(i<-Range(0,10) if(i>5)){
    println(i)
  }
  val fun1=for(i<-Range(0,10)) i*10-1
  println(fun1)
  val fun2=for(i<-Range(0,10)) yield i*10-1
  println("fun2:"+fun2)
}
