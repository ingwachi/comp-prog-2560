# Up Status

ขณะที่เราเล่นเกมเราก็ควรรู้ว่าถ้าเราอัพสเตตัสแล้วค่าพลังต่างๆ ที่เราจะได้ควรเป็นอย่างไรบ้าง
เพียงพอที่จะสามารถใช้สู้กับคนอื่นได้หรือเปล่า โดยจะแบ่งตัวละครเป็นทั้งหมด 3 สาย ได้แก่ 1. เมจ 2. แทงก์ 3. ไฟท์เตอร์
โดยที่แต่ละตัวจะมีคุณสมบัติเฉพาะดังนี้

-   เมจ จะมี Status เริ่มต้น  str=8, int=20, vit=5
-   แทงก์ จะมี Status เริ่มต้น  str=9, int=6, vit=21
-   ไฟท์เตอร์ จะมี Status เริ่มต้น  str=20, int=7, vit=11

Statusในการอัพจะมี 25 points  
ในการอัพ 1 points จะเพิ่มค่า 20 หน่วย  โดยการอัพ status ที่ถูกสายจะเพิ่มค่า +2% ต่อหน่วยโดย
1. หน้าแรกจะแสดง `Welcome!!` และเว้นบรรทัดเป็นการให้เราเลือกสายอาชีพ (ถ้าหากเลือกที่ไม่ได้กำหนดให้บอก `ERROR`)
และให้โชว์สถานะ status bar โดยใน status bar ประกอบด้วยค่า status และแถบพลังจากนั้นจะถามว่าจะอัพ status ไหมเพื่อเป็นการยืนยันในการใช้โปรแกรม  
และถ้าหากตอบว่า "ไม่" ให้ clear โดยให้ใช้คำสั่ง `system(“cls”);` เพื่อเป็นการ clear หน้าจอ (ต้อง `include <stdlib.h>`)
และแสดงผลเป็นคำว่า `ok` เว้น 1 บรรทัดแล้วคำว่า `bye` และให้ใส่คำสั่ง `system("pause");`  
แต่หากตอบว่า "ใช่" จะแสดงผลว่าตอนนี้เรามี Status point ที่ใช้ได้เท่าไหร่ และบรรทัดต่อไปเป็นการป้อนค่าเพื่อทำการอัพ Status แต่ละอันว่าเท่าไหร่จากนั้นให้ clear screen และแสดงหน้าจอสอง
2. หน้าจอสอง แสดงค่า Status bar โดย
แสดงค่าเก่าและค่าใหม่ และใส่คำสั่ง `system("pause");`  
หากอัพเกิน Status point ให้แสดงคำว่า
`Error: your status is Wrong`  
ถ้าหากในหน้านั้นไม่มีการ clear screen ในการแสดงผลใดที่มีบรรทัดไม่น้อยกว่า3 ให้คั่นด้วย `----------`

## ตัวอย่าง Input/Output 
```
Welcome!!
Choose a character
1.Mage 2.Tank 3.Fighter
Select a number[1/2/3]:1
--------------------------
You are Mage!!
An Initial Status is
Str : 8
Int : 20
Vit : 5
Status Points 25
--------------------------
Atk: 160.00
Math: 420.00 		
Def: 100.00
Will do you Up Status? [y/n]: y
---------------------------
Available Points: 25
Up Str : 10
Up Int :  5
Up Vit :  9
```
```
You are Mage!!
Now!! An Initial Status is
Str : 8--->18
Int :  20--->25
Vit : 5--->14
Status Ponits 1
------------------------
Atk: 160.00--->360.0
Matk: 420.00--->510.0
Def: 100.00--->280.0
Press any key to continue...
