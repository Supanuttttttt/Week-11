# การทดลองสัปดาห์ที่ 11  #
# การใช้งาน git ร่วมกับ Visual studio IDE #
---

## 11.3 การทำ Branching ##

16. ในหน้าต่าง Team Explorer  ให้ทำการสร้าง repository  ใหม่ โดยใช้ชื่อว่า EngEdu<p>
<img src = "./images/Fig-3.34.png">

17. ทำการเพิ่ม Solution ให้กับ repository ใช้ชื่อว่า EngEdu 
    <ul>
        <li> ชนิดเป็น Console App (.NET Framework)
        <li> Location คงไว้อย่างที่ปรากฏ
        <li> แก้ไขโปรแกรมให้เป็นดังรูปด้านล่างนี้
    </ul>

<img src = "./images/Fig-3.35.png">

18. ทำการ sync กับ GitHub.com
    <ul>
        <li> ใช้ commit message <b>“first year semester 1”</b>
        <li> ดูการเปลี่ยนแปลงของ repository EngEdu บน GitHub.com
    </ul>    




19. ทำการเพิ่มเติมไฟล์ __Program.cs__ โดยเพิ่มข้อความดังต่อไปนี้<p>
<img src = "./images/Fig-3.36.png">

20. ทำการ sync กับ GitHub.com
    <ul>
        <li> ใช้ commit message <b>“first year semester 2”</b>
        <li> ดูการเปลี่ยนแปลงของ repository EngEdu บน GitHub.com
    </ul>    



เมื่อนักศึกษาเรียนถึงชั้นปีที่ 2 จะต้องมีการแยกแขนงวิชา เพื่อศึกษาในแขนงวิชาที่ตนถนัด หรือต้องการพัฒนาศักยภาพเป็นพิเศษ เมื่อนักศึกษาแยกแขนงออกมาแล้ว ก็จะต้องเรียนในวิชาของแขนงวิชาเป็นหลัก แต่จะยังคงมีนักศึกษาบางส่วน ที่พักการเรียนในบางวิชาของปี 1 เทอม 1  จึงต้องลงทะเบียนใน ปี 2 เทอม 1 ซึ่งจะยังคงเดินตามแผนการศึกษาในรายวิชาของภาควิชาต่อไป (เรียกชื่อ branch นี้ว่า  master) 
ทำนองเดียวกัน ในการพัฒนาซอฟต์แวร์ เมื่อได้วางตลาดรุ่นที่ 1.0 แล้ว ก็อาจจะต้องมีการพัฒนา features เพิ่มเติม เป็นรุ่น 1.1, 1.2, … หรือรุ่น 2.0 สิ่งหนึ่งที่นักพัฒนาต้องพบกับความยุ่งยากคือ การพัฒนารุ่นใหม่ ไปพร้อมๆ กับการแก้บักของรุ่นเก่า จะเกิดความยุ่งยากในการรักษา code เพื่อไม่ให้ code ของแต่ละรุ่นหรือแต่ละความมุ่งหมายในการพัฒนารบกวนกัน ความสามารถด้าน branching ของ Git จึงเข้ามามีบทบาทสำคัญ
 
 

<table>
<tr> 
<td valign="top" width = "50%">21. การแยก branch ใน Visual Studio
    <ul>
        <li> ในหน้าต่าง Team Explorer ให้คลิกที่ Home และ Branches (อยู่ภายใต้หัวข้อ Project)
    </ul>    
</td>
<td valign="top"><img src = "./images/Fig-3.37.png"> </p> </td>
</tr>
</table>

<table>
<tr> 
<td valign="top"  width = "50%">22. ภายใต้หัวข้อ  Active Git Repositories จะพบว่ามี Repo ของเราตามด้วย (master) และมี branch ที่ชื่อว่า master เป็นโหนดลูก แสดงเป็นตัวหนา
    <ul>
        <li> คลิกขวาที่ branch master
        <li> เลือก New Local Branch From...
    </ul>    
</td>
<td valign="top"><img src = "./images/Fig-3.38.png"> </p> </td>
</tr>
</table>

<table>
<tr> 
<td valign="top"  width = "50%">23. ตั้งชื่อ  Branch
    <ul>
        <li> ใส่ชื่อ Branch เป็น Computer
        <li> คลิก Create Branch
    </ul>    
สังเกตว่า ในโหนด Engedu จะมีการแสดงเป็น  EngEdu (Computer) และโหนดลูกที่ชื่อ Computer จะเปลี่ยนเป็นตัวหนาขณะที่ master กลายเป็นตัวปกติ นั่นคือ ขณะนี้ เราได้ย้ายไปทำงานใน branch ที่ชื่อ Computer
  
<p><p>
<b>***** การเปลี่ยนแปลงใด ๆ จะถูกกระทำภายใต้ branch ปัจจุบัน (ที่แสดงด้วยตัวหนา) เท่านั้น ***** </b>
<p><p>
    
การเปลี่ยน branch ทำได้ง่ายๆ โดยการ double  click ที่ชื่อ branch 

<b>***** ทุกครั้งที่มีการเปลี่ยน branch </b>
1. git จะลบไฟล์ทั้งหมดใน working directory 
2. git จะทำการ checkout ไฟล์ใน branch ปัจจุบันออกมาทำงาน  แทนไฟล์ทั้งหมดใน working directory

</td>
<td valign="top"><img src = "./images/Fig-3.39.png"> </p> </td>
</tr>
</table>

 
24. ทำให้แน่ใจว่า เรากำลังทำงานกับ Branch ที่ชื่อ  Computer 
    <ul>
        <li>ในโหนด Engedu จะต้องแสดงเป็น  EngEdu (Computer) และโหนดลูกที่ชื่อ Computer จะต้องเป็นตัวหนา
        <li>แก้โปรแกรมเป็นดังต่อไปนี้ 
    </ul>
<img src = "./images/Fig-3.40.png">


25. ทำการ sync กับ GitHub.com
    <ul>
        <li>ใช้ commit message <b>"2nd  year semester 1"</b>
        <li>ดูการเปลี่ยนแปลงของ repository EngEdu บน GitHub.com
        <li><b>กรณีที่ Sync  ไม่สำเร็จ ให้ลองใช้การ push เนื่องจากในขณะนี้ ยังไม่มี branch ที่ชื่อ Computer บน GitHub.com</b>
    </ul>


26. เปลี่ยน Branch กลับไปยัง master โดยการ double click ที่ master
    <ul>
        <li>สังเกตุการเปลี่ยนแปลงที่เกิดขึ้นกับไฟล์ Program.cs
        <li>ทดลองสลับไปมาระหว่าง branch ที่ชื่อ master และ Computer (โดยการ double click)
    </ul>



27. ทำให้แน่ใจว่า เรากำลังทำงานกับ Branch ที่ชื่อ  master
    <ul>
        <li>ในโหนด Engedu จะต้องแสดงเป็น  EngEdu (master) และโหนดลูกที่ชื่อ master จะต้องเป็นตัวหนา
        <li>แก้โปรแกรมเป็นดังต่อไปนี้ 
    </ul>
<img src = "./images/Fig-3.41.png">

<p>

28. ทำการ sync กับ GitHub.com
    <ul>
        <li>ใช้ commit message “2nd  year semester 1”
        <li>ดูการเปลี่ยนแปลงของ repository EngEdu บน GitHub.com
        <li><b>กรณีที่ Sync  ไม่สำเร็จ ให้ลองใช้การ push เนื่องจากในขณะนี้ ยังไม่มี branch ที่ชื่อ Computer บน GitHub.com</b>

    </ul>

29. เปลี่ยน Branch กลับไปยัง Computer โดยการ double click ที่ Computer
    <ul>
        <li>สังเกตุการเปลี่ยนแปลงที่เกิดขึ้นกับไฟล์ Program.cs
        <li>ทดลองสลับไปมาระหว่าง branch ที่ชื่อ master และ Computer (โดยการ double click)
    </ul>
