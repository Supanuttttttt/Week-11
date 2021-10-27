# การทดลองสัปดาห์ที่ 11  #
# กรณึศึกษา การสร้างโปรแกรม My Transcript #

## Branch 3 เพิ่มคลาส course เพื่อบันทึกรายวิชาและเกรด ##
---

1. ในหน้าต่างของ Form1.cs[Design] ให้เรียกเมนู View->Code หรือกด F7 เพื่อทำการแก้ไข code
<p> <img src = "./images/Fig_CaseStudy_18.png">

2. เพิ่มคลาส Course ลงในตำแหน่งดังรูป <br>(อย่าไปไว้เหนือคลาส Form1 เพราะอาจจะทำให้หน้าต่างที่ใช้แก้ไข Form เกิดปัญหาได้)
<p> <img src = "./images/Fig_CaseStudy_19.png">

#### Source code สำหรับคลาส Course ####
``` cs
class Course
{
    public string CourseID { get; set; }
    public string CourseName { get; set; }
    public string CourseCredit { get; set; }
    public string Grade { get; set; }
}
```

