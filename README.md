# การทดลองสัปดาห์ที่ 11  #
# การใช้งาน git ร่วมกับ Visual studio IDE #
---
### การติดตั้ง IDE (Microsoft Visual Studio Community Edition) ###

การทดลองนี้จะใช้ Microsoft Visual Studio Community Edition ดังนั้นหากนักศึกษายังไม่ได้ติดตั้ง ให้ดำเนินการติดตั้งให้เรียบร้อย โดยมี component สำคัญที่ต้องติดตั้งคือ Git for Windows ดังเอกสารแนะนำต่อไปนี้
*  [การติดตั้ง IDE (Microsoft Visual Studio Community Edition)](./VS-Installation.md)

---
### หัวข้อการทดลอง ###

 [1. การสร้าง repository บน GitHub ด้วย Visual Studio](./Week_11_Exp_1_git_repo_create_on_VS.md)

 [2. การ clone จาก repository ด้วย Visual Studio](./Week_11_Exp_2_git_clone_on_VS.md)

 [3. การสร้าง repository บน GitHub ด้วย Visual Studio](./Week_11_Exp_3_git_branching.md)

---


### แบบฝึกหัด
ให้ทำการเพิ่ม commit ตามภาคการศึกษาต่างๆ โดยเขียน Hilight ที่นักศึกษาคิดว่าที่จะพบในแต่ละภาคการศึกษา จนถึงชั้นปีที่ 4 ภาคเรียนที่ 2

เมื่อเราพัฒนาซอฟต์แวร์ โดยการแยก branch และคิดว่าถึงจุดหนึ่งที่สามารถนำไปรวมกับ master ได้ เราจะต้องทำการ merge เพื่อรวม branch เข้าด้วยกัน ซึ่งการ merge นี้ระบบของ git จะทำการตรวจเช็คให้ด้วย ว่าสามารถ merge ได้หรือไม่

30. การรวม Branch (merge)
    <ul>
        <li>ทำให้แน่ใจว่าอยู่ที่ Branch ปลายทางที่จะทำการ merge  ในที่นี้คือ master ดังนั้น ที่โหนด  EngEdu ต้องแสดงเป็น EngEdu (master) และโหนดลูก master ต้องเป็นตัวหนา
        <li>คลิกขวาที่โหนดลูก เลือก Merge From… จากเมนูป๊อบอับ
    </ul>
<img src = "./images/Fig-3.42.png">

<p>
    
<table>
<tr> 
<td valign="top"  width = "50%">31. ทำการ merge
    <ul>
        <li> Merge from branch : Computer 
        <li> Into current branch: master
        <li> คลิก Merge
    </ul>    
</td>
<td valign="top"><img src = "./images/Fig-3.43.png"> </p> </td>
</tr>
</table>

<p>
    
<table>
<tr> 
<td valign="top" width = "50%">32. Merge conflict<p>
ในการ merge เราจะพบว่า บางครั้งมีการแก้ไข source code ที่หมายเลขบรรทัดเดียวกัน บนไฟล์เดียวกัน กรณีนี้เรียกว่าเกิดการขัดแย้ง
เราต้องดำเนินการอย่างใดอย่างหนึ่ง เพื่อจัดการกับความขัดแย้งนั้น เพื่อให้สามารถดำเนินการพัฒนาซอฟต์แวร์ต่อไปได้
ถ้าเจอสถานการณ์นี้ ให้คลิก Conflict: 1</td>
<td valign="top"><img src = "./images/Fig-3.44.png"> </p> </td>
</tr>
</table>


    
<p>
    
<table>
<tr> 
<td valign="top" width = "50%">33. การแก้ไข Merge conflict<p>
    ในการ merge เราจะพบว่า บางครั้งมีการแก้ไข source code ที่หมายเลขบรรทัดเดียวกัน บนไฟล์เดียวกัน กรณีนี้เรียกว่าเกิดการขัดแย้ง
ให้คลิกที่ชื่อไฟล์ที่ขัดแย้งนั้น จะพบว่า เราสามารถแก้ไขได้ในหลายรูปแบบเช่น
<ol>
    <li> ยกเลิกการ merge โดยการคลิกที่  Undo Merge </li>
    <li> เปรียบเทียบความแตกต่างระหว่างไฟล์ทั้งสอง โดยการคลิกที่ Compare file
    <li> เข้าไปแก้ไขไฟล์ใน branch ปลายทาง
    <li> เข้าไปแก้ไขไฟล์ที่นำมา merge
</ol>

ให้นักศึกษาทดลองคลิกที่ตัวเลือกต่างๆ 

__ถ้าต้องการกลับไปก่อนการ merge ให้กด Undo merge__</td>
<td valign="top"><img src = "./images/Fig-3.45.png"> </p> </td>
</tr>
</table>


34. ดูผลการเปลี่ยนแปลงหลังจากการ merge
    <ul>
        <li> สังเกตุการเปลี่ยนแปลงที่เกิดขึ้นกับไฟล์ Program.cs
        <li> ทดลองสลับไปมาระหว่าง branch ที่ชื่อ master และ Computer (โดยการ double click)
    </ul>    


## คำถาม

<ol>
<li> ในกรณีที่ต้องการรักษา source code ของทั้งสองไฟล์ไว้ ควรทำอย่างไร
<li> ผลของการ keep target ออกมาเป็นอย่างไร
<li> ผลของการ take source ออกมาเป็นอย่างไร
<li> ให้ capture หน้าจอของ Compare files, Diff ที่ source, Diff ที่ target
</ol>

__หมายเหตุ หากนักศึกษาทำการทดลองเพื่อที่จะตอบคำถามข้างต้น แล้วทำให้เกิดผลที่ไม่คาดคิด ให้กด `Undo merge`__


