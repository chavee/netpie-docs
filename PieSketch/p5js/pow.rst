.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

pow()
=====

อำนวยความสะดวกในการแสดงออกที่เป็นเอกลัษณ์ ฟังก์ชัน pow () เป็นวิธีที่มีประสิทธิภาพในการคูณตัวเลขด้วยตัวเอง (หรือสิ่งตอบแทน) ในปริมาณมาก ยกตัวอย่างเช่น pow (3, 5) เทียบเท่ากับการแสดงออก 3 * 3 * 3 * 3 * 3 และ pow (3, -5) เท่ากับ 1/3 * 3 * 3 * 3 * 3 Maps to Math.pow ()

.. Facilitates exponential expressions. The pow() function is an efficient
.. way of multiplying numbers by themselves (or their reciprocals) in large
.. quantities. For example, pow(3, 5) is equivalent to the expression
.. 3*3*3*3*3 and pow(3, -5) is equivalent to 1 / 3*3*3*3*3. Maps to
.. Math.pow().

**รูปแบบการใช้งาน**

pow ( n, e )

**พารามิเตอร์**

- ``n``  Number: ฐานของนิพจน์เลขชี้กำลัง

- ``e``  Number: พลังที่จะยกฐาน

.. ``n``  Number: base of the exponential expression
.. ``e``  Number: power by which to raise the base

**ค่าที่ส่งออกมา**

- Number: n ^ อี

.. Number: n^e

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	function setup() {
	  //Exponentially increase the size of an ellipse.
	  eSize = 3; // Original Size
	  eLoc = 10; // Original Location
	
	  ellipse(eLoc, eLoc, eSize, eSize);
	
	  ellipse(eLoc*2, eLoc*2, pow(eSize, 2), pow(eSize, 2));
	
	  ellipse(eLoc*4, eLoc*4, pow(eSize, 3), pow(eSize, 3));
	
	  ellipse(eLoc*8, eLoc*8, pow(eSize, 4), pow(eSize, 4));
	}

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
