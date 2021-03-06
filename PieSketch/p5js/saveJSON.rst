.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

saveJSON()
==========

เขียนเนื้อหาของอาร์เรย์หรือวัตถุ JSON เป็นไฟล์. json กระบวนการบันทึกไฟล์และตำแหน่งของไฟล์ที่บันทึกไว้จะแตกต่างกันไปในแต่ละเว็บเบราเซอร์

.. Writes the contents of an Array or a JSON object to a .json file.
..  The file saving process and location of the saved file will
..  vary between web browsers.

**รูปแบบการใช้งาน**

saveJSON ( json, filename, [optimize] )

**พารามิเตอร์**

- ``json``  Array,Object: 

- ``filename``  String: 

- ``optimize``  Boolean: ถ้าเป็นจริงให้เอาเส้นแบ่งและช่องว่างออกจากไฟล์ที่ส่งออกเพื่อเพิ่มประสิทธิภาพไฟล์ (แต่ไม่สามารถอ่านได้)

.. ``json``  Array,Object: 
.. ``filename``  String: 
.. ``optimize``  Boolean: If true, removes line breaks and spaces from the output file to optimize filesize (but not readability).

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	 var json;
	
	 function setup() {
	
	   json = {}; // new JSON Object
	
	   json.id = 0;
	   json.species = 'Panthera leo';
	   json.name = 'Lion';
	
	 // To save, un-comment the line below, then click 'run'
	 // saveJSON(json, 'lion.json');
	 }
	
	 // Saves the following to a file called "lion.json":
	 // {
	 //   "id": 0,
	 //   "species": "Panthera leo",
	 //   "name": "Lion"
	 // }
	 

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
