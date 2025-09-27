คู่มือ: การสร้างและ Inject HbbTV AIT เข้า MUX DVB-T2
1. ความเข้าใจเบื้องต้น
•	AIT (Application Information Table): ตารางพิเศษใน DVB ใช้ประกาศว่า service ใดมี HbbTV application อยู่, URL ของแอปคืออะไร, ควร autostart หรือกดปุ่มแดงถึงจะขึ้น
•	PMT (Program Map Table): ตารางที่อธิบายว่า Service (ช่อง) มีองค์ประกอบอะไรบ้าง เช่น Video, Audio, Subtitles รวมถึง AIT (ซึ่งประกาศเป็น private stream type 0x05)
•	การ inject AIT = ทำให้กล่อง/ทีวีรู้จักว่าช่องมี HbbTV app
________________________________________
2. ไฟล์ที่ใช้
•	bbc/mux.ts → ไฟล์ TS ของ Freeview (อังกฤษ) ที่มี AIT ของ BBC ONE HD (ใช้เป็นตัวอย่างอ้างอิง)
•	mcot/mux.ts → ไฟล์ TS ของ MUX MCOT (ประเทศไทย) ที่จะนำมาทดลองใส่ AIT
•	mcot_ait.xml → ไฟล์ XML ของ AIT ที่เราสร้างเอง ชี้ไปที่ HbbTV app ของ MCOT (http://radiostl3.mcot.net/hbbtv/default.html)
•	mcot_pmt.xml → ไฟล์ XML ของ PMT ของ 9MCOT HD (ดึงจาก TS และแก้ไขเพิ่ม component AIT)
