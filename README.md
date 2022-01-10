# MMNbot

MMNbot คือ บอทของ Discord มีจุดประสงค์คือ ใช้ในการเปิดเพลงจากลิ้ง URL ของ youtube  
สามารถเปิดเพลงแบบเป็น playlist ได้  
MMNbot เขียนโดยใช้ภาษา Python โดยใช้ไลบารี่ discord.py  
ถ้าอยากเชิญบอทเข้าเซิฟเวอร์ Discord ให้[กดที่นี้](https://discord.com/api/oauth2/authorize?client_id=867733364693270528&permissions=3147776&redirect_uri=https%3A%2F%2Fdiscord.events.stdlib.com%2Fdiscord%2Fauth%2F&scope=bot)

## หลักการทำงาน 

ตัว MMNbot นี้จะมีเครื่องมือที่ใช้หลักๆอยู่ 4 ตัว คือ  
-Discord.py เป็น Libraryที่ใช้ในการติดต่อสื่อสารระหว่างcode กับDiscord โดยใช้ Discord API  
-YouTube dl เป็น Libraryที่ใช้ในการดาวน์โหลดหรือ Streaming วีดีโอจาก YouTube  
-YouTube data api เป็น api ของ youtube ที่ใช้ในการจัดการข้อมูลต่างๆของ Youtube
-FFmpeg เป็นโปรแกรมที่ใช้ในการจัดการสื่อ Multimedia ต่างๆ  

หลักการทำงานคร่าวๆ ของ MMNbot คือ  
เมื่อผู้ใช้วางLinkURL หรือชื่อเพลงแล้ว ตัวyoutube api จะนำLinkURL มาแปลงเป็นข้อมูลในการ  Steaming แต่ถ้าเป็นชื่อเพลงจะใช้ youtube dl ในการค้นหา แล้วแปลงให้เป็น LinkURL  
แล้วค่อยส่งให้ youtube api ในการดาวน์โหลดข้อมูลSteaming อีกที  
หลังจากนั้นก็จะส่งข้อมูล Steamingที่ได้ ไปให้FFmpeg เพื่อให้ FFmpeg Steamingเพลง  
โดยผ่าน discord.py  


## คำสั่งของ MMNbot

```prefix``` ของMMNbot คือ ```!```

```p```  หรือ ```play``` ตามด้วย ```URL ของ Youtube``` หรือ```ชื่อเพลง``` :เปิดเพลง  
```sp``` หรือ ```skip``` : ข้ามเพลงที่กำลังเล่นอยู่ตอนนี้  
```ls``` หรือ ```lists``` : คิวเพลงที่มีอยู่ตอนนี้  
```pu``` หรือ ```pause``` : ให้หยุดเล่นเพลงชั่วคร่าว  
```re``` หรือ ```resume``` : เล่นเพลงต่อ  
```cl``` หรือ ```clear``` : ลบคิวเพลงทั้งหมด  
```le``` หรือ ```leave``` : เอาบอทออกจากห้องเสียง  


สำหรับฟังก์ชันของ MMNbotในตอนนี้ มีอยู่เท่านี้แต่ในอนาคตจะมีการพัฒนาเพิ่มมาอีกเรื่อยๆ


