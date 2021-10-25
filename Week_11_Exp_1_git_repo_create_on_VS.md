# การทดลองสัปดาห์ที่ 11  #
# การใช้งาน git ร่วมกับ Visual studio IDE #
---


## 11.1 การสร้าง repository บน GitHub ด้วย Visual Studio ##

<table>
<tr> 
<td valign="top"  width = "50%">ในแท็บ Team Explorer ให้สร้าง repository โดยการคลิกปุ่ม <b>Create</b></td>
<td valign="top "><img src = "./images/Fig-3.20.png"> </p> </td>
</tr>
</table>  

<table>
<tr> 
<td valign="top"  width = "50%">ระบุรายละเอียดของ repo ใหม่ที่จะสร้าง
<ul>
  <li> ในช่อง Name ให้เพิ่มชื่อ repository  <b>CL64-xxx-week11</b>
  <span style="color:blue">โดย xxx คือเลขสามตัวท้ายของรหัสนักศึกษา</span>
  <li> ในช่อง Description ให้ใส่รายละเอียดสั้นๆ  <b>Computer Laboratory 1 :  week 11</b>
  <li> ในช่อง Local path ให้ใส่ path ไปยังงานที่เคยทำไว้แต่อยู่ใน folder หลักเดียวกัน เช่น ถ้างานเดิม c:\Code\CL60-02 ให้ใส่เป็น  <b>c:\Code\CL64-xxx-week11</b>
  <li> ในช่อง Git ignore และ License คงไว้อย่างที่ปรากฏ
  <li> กดปุ่ม <b>Create</b>
</ul>
</td>
<td valign="top"><img src = "./images/Fig-3.21.png"> </p> </td>
</tr>
</table>  

 


### เมื่อสร้างเสร็จ ให้ตรวจสอบรายการ repository ที่เพิ่มขึ้นบน GitHub.com

<table>
<tr> 
<td valign="top"  width = "50%">3. เพิ่ม solution ใหม่ไปยัง repository<br>
คลิกที่ New… จะปรากฏหน้าต่าง ให้สร้าง Solution ใหม่ ให้ทำตามข้อ 4
</td>
<td valign="top"><img src = "./images/Fig-3.22.png"> </p> </td>
</tr>
</table>

4. ใส่รายละเอียดของ Solution  ใหม่ที่ต้องการสร้าง

<img src = "./images/Fig-3.23.png">

5. เมื่อ Solution ใหม่ถูกสร้างขึ้นมา ให้แก้ไข code ตามรูปต่อไปนี้
<img src = "./images/Fig-3.24.png">

  
<table>
<tr> 
<td valign="top" width = "50%">6. เมื่อ แก้ไขเสร็จ ให้คลิกที่ Changes เพื่อดูการเปลี่ยนแปลง เทียบได้กับการสั่ง git status
</td>
<td valign="top"><img src = "./images/Fig-3.25.png"> </p> </td>
</tr>
</table>

<table>
<tr> 
<td valign="top" width = "50%">7. Team Explorer จะรายงานไฟล์ที่มีการเปลี่ยนแปลง พร้อมทั้งมีช่่องให้ใส่ข้อความสำหรับการ  commit  เมื่อกรอกข้อความเสร็จให้คลิกปุ่ม Commit All
</td>
<td valign="top" ><img src = "./images/Fig-3.26.png" > </p> </td>
</tr>
</table>




การสั่ง Commit All จะเป็นการเก็บบันทึกการเปลี่ยนแปลงที่แสดงในรูปไว้ใน Local repository ถ้าหากเราต้องการบันทึกการเปลี่ยนแปลงไว้บนเวบ GitHub จะต้องทำการ Sync  ซึ่งคำสั่ง Sync  นี้จะทำการ pull และ push ให้เราโดยอัตโนมัติทั้ง 2 คำสั่ง

<table>
<tr> 
<td valign="top" width = "50%" >8. ให้ทำการ sync repo ที่เราสร้างขึ้นไปบน Github</td>
<td valign="top" ><img src = "./images/Fig-3.27.png"> </p> </td>
</tr>
</table>




#### ++เมื่อ sync เสร็จ ให้ตรวจสอบรายการไฟล์ใน repository บน GitHub.com++ ###

---
