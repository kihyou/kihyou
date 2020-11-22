---
layout: post
title: "4. Java输入和输出"
date: 2020-11-18
category: Java
---
输入输出语句
输入语句
import java.util.Scanner;//导包
Scanner sc = new Scanner(System.in);//创建Scanner对象
//int a = sc.nextInt();
//String s = sc.next();
String s = sc.nextLine();
sc.close();
输出语句
System.print()            ——输出
System.out.println()    ——输出并换行
垃圾自动回收机制
object 01 = new object();
object 02 = new object();
02 = 01;
01 = null;
System. out . println(o2);
//垃圾自动回收机制
// Java GC(garbage collec, 垃圾收集,回收)
输入输出流（IO流）
I:input         输入
0:output     输出
类型:
字节流( InputStream/ OutputStream)
字节，绝大部分数据文件，图片音频视频
InputStream
>
try {
                //创建流
                FileInputStream fr = new FileInputStream("d:/aa/b1. txt");
                //读取
                byte[] data = new byte[1024];// 定义数组缓冲区，用于存放读取来的内容
                int i = fr.read(data);// 执行读取操作，获取读取内容的有效长度
                System . out. println(i);
                // i = fr.read(data);//-1
                // System. out . println(i);
                data = Arrays. copyOf(data, i);// 根据有效长度截图数组内容。
                System. out . println(new String(data));// 输出内容到控制台中。
                //关闭流
        } catch (FileNotFoundException e) {
                // TODO Auto-generated catch block
                e.printStackTrace();
            } catch (IOException e) {
                // TODO Auto-generated catch block
                e.printStackTrace();
            }
OutputStream
FileOutpitStream
        String name = UUID.randomUUID().toString();
        System.out.println(name);
        try {
            FileOutputStream fw = new FileOutputStream("d:/" + name + ".txt");
            fw.write(" abcdefg".getBytes());
            fw.close();
        } catch (Exception e) {
            e.printStackTrace();

        }
字符流( Reader/Writer)
以字符的形式，字符文本类型的数据读写操作:
Reader
InputStreamReader
FileReader
try {
  // 创建流
  FileReader fr = new FileReader("d:/a/a.txt");
  // 读取
  char[] data = new char[108];// 定义数组缓冲区，用于存放读取来的内容。
  int i = fr.read(data); // 执行读取操作，获取读取内容的有效长度
  System.out.println(i);
  data = Arrays.copyOf(data, i);// 根据有效长度截图数组内容。
  System.out.println(data.length);
  System.out.println(new String(data));// 输出内容到控制台中。
  // 关闭流
  fr.close();
  } catch (FileNotFoundException e) {
      // TODO Auto-generated catch block
      e.printStackTrace();
  } catch (IOException e) {
      // TODO Auto-generated catch block
      e.printStackTrace();
  } catch (Exception e) {
      // TODO Auto-generated catch block
      e.printStackTrace();
BufferReader
Writer
OutputStreamWriter
FileWriter
//创建流
try {
  FileWriter fw = new FileWriter("d:/aa/b1.txt");//默认false
  //读/写操作
  fw.write("\tafasdfewffds");//文件不存在会报异常
  //关闭流
  fw.close();
}catch (FileNotFoundException e) {
      e.printStackTrace();
  } catch (IOException e) {
      e.printStackTrace();
  } catch (Exception e) {
      e.printStackTrace();
  }
基本使用-核心本质:
创建流
读/写
关闭流
终端流
直接与终端目标打交道
拼接流
直接与流打交道，从构造方法中可以看出来。
拼接流与终端流需要注意流向一致的问题。
相对/绝对路径
public static void main(String[] args) {
        System.out.println(File.separatorChar);
        // 对于UNIX/Linux平台，绝对路径名的前缀是"/"。
        // 相对路径名没有前缀。
        //
        // 对于Windows平台，
        // 绝对路径名的前缀由驱动器号和一个”:"组成，
        // 例"c:\..."。
        // 相对路径没有盘符前缀。
        //
        // 相对路径:
        // 指相对于某位置的路径，是指相对于当前目录。
        File f1 = new File("a.txt");
        System.out.println(f1.getAbsoluteFile());
        System.out.println(f1.getPath());
        File f2 = new File("d:\\c\\a.txt");
        System.out.println(f2.getAbsolutePath());
        System.out.println(f2.getPath());
        // 一般在使用时，建议用绝对路径，
        // 因为相对路径容易出问题，不好确定到底在什么地方。
            File f3 = new File("src/a. txt");
            System.out.println(f3.getAbsolutePath());
            System.out.println(f3.getPath());
   }
顺序
        try {
            // 创建流
            FileReader fr = new FileReader("d:/aa/b1.txt");
            BufferedReader br = new BufferedReader(fr);
            String s = br.readLine();
            System.out.println(s);

            // s = br.readLine(); :
            // System. out . println(s);
            // 关闭流-**顺序**
            br.close();
            fr.close();
            br = null;
            fr = null;
        } catch (FileNotFoundException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        } catch (IOException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        }
复制文件
public static void main(String[] args) {
        // TODO Auto-generated method stub
        try {
            FileInputStream fi = new FileInputStream("D:\\Users\\kihyou\\Desktop\\b.jpg");
            FileOutputStream fo = new FileOutputStream("D:/0/b.png");
            byte[] data = new byte[1024];
            fo.write(data);
            fi.close();
            fo.close();
            System.out.println("复制完成");
        } catch (FileNotFoundException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        } catch (IOException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        }
    }
>
复制文件夹
import java.io.*;

public class Test02 {

    public static void main(String[] args) {
        // TODO Auto-generated method stub
        try {
            FileInputStream fi = new FileInputStream("D:\\Users\\kihyou\\Desktop\\b.jpg");
            FileOutputStream fo = new FileOutputStream("D:/0/b.png");
            byte[] data = new byte[1024];
            fo.write(data);
            fi.close();
            fo.close();
            System.out.println("复制完成");
        } catch (FileNotFoundException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        } catch (IOException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        }
    }

    public void f1() throws IOException {
        File fin = new File("D:/aa/a1");
        File fout = new File("D:/aa/a2");
        File[] finList = fin.listFiles();
        for (File f : finList) {
            to(f, fout);
        }
    }

    public void to(File in, File out) throws IOException {
        FileInputStream fr = new FileInputStream(in);
        String name = out.getAbsolutePath() + "/" + in.getName();
        FileOutputStream fw = new FileOutputStream(name);
        byte[] data = new byte[1024];
        int i;
        while (-1 != (i = fr.read(data))) {
            fw.write(data);
        }
        fr.close();
    }

}
>
序列化与反序列化
public class Test30M1 implements Serializable{

    private static final long serialVersionUID = 1L;
    private int i = 1;
    private int a = 1;
    private String S = "SS";
    public int getI() {
        return i;
    }
    public void setI(int i) {
        this.i = i;
    }
    public int getA() {
        return a;
    }
    public void setA(int a) {
        this.a = a;
    }
    public String getS() {
        return S;
    }
    public void setS(String s) {
        S = s;
    }
    public static long getSerialversionuid() {
        return serialVersionUID;
    }

}
>
        List<Test30M1> l1 = new ArrayList<Test30M1>();
        Test30M1 m = new Test30M1();
        m.setI(10);
        m.setS("a");
>
序列化/持久化
try {
            FileOutputStream fw= new FileOutputStream("D:\\Users\\kihyou\\Desktop\\b.txt");
            ObjectOutputStream os = new ObjectOutputStream(fw);
            os.writeObject(m);
            os.close();
            fw.close();
        } catch (FileNotFoundException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        } catch (IOException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        }
>
反序列化
try {
            //创建流
            FileInputStream fr = new FileInputStream("D:\\Users\\kihyou\\Desktop\\b.txt");
            ObjectInputStream os = new ObjectInputStream(fr);
            //读取
            Object o = os .readObject();//反序列化
             // if (o instanceof List) {
            // List<Test30M1> m = (List<Test30M1>) 0;
            // System. out . println(m.size());
            //}|”
            if (o instanceof Test30M1) {
            Test30M1 m = (Test30M1) o;
            System. out . println(m. getS());
            }
            //关闭流
            os. close();
            fr.close();
        } catch (FileNotFoundException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        } catch (ClassNotFoundException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        } catch (IOException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        }
>
部分属性的序列化
try {
            // 创建流
            FileInputStream fr = new FileInputStream("d:/a/a. txt");
            ObjectInputStream os = new ObjectInputStream(fr);
            // 读取
            Object o = os.readObject();
            // if (o instanceof List) {
            // List<Test30M1> m = (List<Test30M1>) 0;
            // System. out . println(m.size());
            // }
            if (o instanceof Test30M1) {
                Test30M1 m = (Test30M1) o;
                System.out.println(m.getS());
                // 关闭流
                os.close();
            }
        } catch (FileNotFoundException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        } catch (ClassNotFoundException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        } catch (IOException e) {
            // TODO Auto-generated catch block
            e.printStackTrace();
        }
    }
