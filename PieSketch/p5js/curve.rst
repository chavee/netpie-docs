.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

curve()
=======

วาดเส้นโค้งบนหน้าจอระหว่างสองจุดให้เป็นสี่พารามิเตอร์กลาง พารามิเตอร์สองตัวแรกเป็นจุดควบคุมราวกับว่าเส้นโค้งมาจากจุดนี้ถึงแม้ว่าจะไม่วาดก็ตาม พารามิเตอร์สองตัวสุดท้ายอธิบายจุดควบคุมอื่น ๆ ในทำนองเดียวกัน  เส้นโค้งที่ยาวขึ้นสามารถสร้างขึ้นได้โดยการใช้ชุดของฟังก์ชัน curve () ร่วมกันหรือใช้ curveVertex () ฟังก์ชันเพิ่มเติมที่เรียกว่า curveTightness () ให้การควบคุมคุณภาพภาพของเส้นโค้ง ฟังก์ชัน curve () คือการดำเนินการ Splines Catmull-Rom

.. Draws a curved line on the screen between two points, given as the
.. middle four parameters. The first two parameters are a control point, as
.. if the curve came from this point even though it's not drawn. The last
.. two parameters similarly describe the other control point. 
.. Longer curves can be created by putting a series of curve() functions
.. together or using curveVertex(). An additional function called
.. curveTightness() provides control for the visual quality of the curve.
.. The curve() function is an implementation of Catmull-Rom splines.

**รูปแบบการใช้งาน**

curve ( x1, y1, x2, y2, x3, y3, x4, y4 )

**พารามิเตอร์**

- ``x1``  Number: พิกัด x สำหรับจุดควบคุมจุดเริ่มต้น

- ``y1``  Number: พิกัด y สำหรับจุดควบคุมจุดเริ่มต้น

- ``x2``  Number: พิกัด x สำหรับจุดแรก

- ``y2``  Number: พิกัด y สำหรับจุดแรก

- ``x3``  Number: พิกัด x สำหรับจุดที่สอง

- ``y3``  Number: y พิกัดสำหรับจุดที่สอง

- ``x4``  Number: พิกัด x สำหรับจุดควบคุมจุดสิ้นสุด

- ``y4``  Number: y- พิกัดสำหรับจุดสิ้นสุดการควบคุม

.. ``x1``  Number: x-coordinate for the beginning control point
.. ``y1``  Number: y-coordinate for the beginning control point
.. ``x2``  Number: x-coordinate for the first point
.. ``y2``  Number: y-coordinate for the first point
.. ``x3``  Number: x-coordinate for the second point
.. ``y3``  Number: y-coordinate for the second point
.. ``x4``  Number: x-coordinate for the ending control point
.. ``y4``  Number: y-coordinate for the ending control point

**ค่าที่ส่งออกมา**

- p5: วัตถุ p5

.. p5: the p5 object

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	noFill();
	stroke(255, 102, 0);
	curve(5, 26, 5, 26, 73, 24, 73, 61);
	stroke(0);
	curve(5, 26, 73, 24, 73, 61, 15, 65);
	stroke(255, 102, 0);
	curve(73, 24, 73, 61, 15, 65, 15, 65);

	</script>

	<br><br>

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	// Define the curve points as JavaScript objects
	p1 = {x: 5, y: 26}, p2 = {x: 73, y: 24}
	p3 = {x: 73, y: 61}, p4 = {x: 15, y: 65}
	noFill();
	stroke(255, 102, 0);
	curve(p1.x, p1.y, p1.x, p1.y, p2.x, p2.y, p3.x, p3.y)
	stroke(0);
	curve(p1.x, p1.y, p2.x, p2.y, p3.x, p3.y, p4.x, p4.y)
	stroke(255, 102, 0);
	curve(p2.x, p2.y, p3.x, p3.y, p4.x, p4.y, p4.x, p4.y)

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
