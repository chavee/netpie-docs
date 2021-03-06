.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

fromAngle()
===========

สร้างเวกเตอร์แบบ 2D ใหม่จากมุมหนึ่ง

.. Make a new 2D unit vector from an angle

**รูปแบบการใช้งาน**

fromAngle ( angle )

**พารามิเตอร์**

- ``angle``  Number: มุมที่ต้องการ

.. ``angle``  Number: the desired angle

**ค่าที่ส่งออกมา**

- p5.Vector: วัตถุ p5.Vector ใหม่

.. p5.Vector: the new p5.Vector object

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	function draw() {
	  background (200);
	
	  // Create a variable, proportional to the mouseX,
	  // varying from 0-360, to represent an angle in degrees.
	  angleMode(DEGREES);
	  var myDegrees = map(mouseX, 0,width, 0,360);
	
	  // Display that variable in an onscreen text.
	  // (Note the nfc() function to truncate additional decimal places,
	  // and the "\xB0" character for the degree symbol.)
	  var readout = "angle = " + nfc(myDegrees,1,1) + "\xB0"
	  noStroke();
	  fill (0);
	  text (readout, 5, 15);
	
	  // Create a p5.Vector using the fromAngle function,
	  // and extract its x and y components.
	  var v = p5.Vector.fromAngle(radians(myDegrees));
	  var vx = v.x;
	  var vy = v.y;
	
	  push();
	  translate (width/2, height/2);
	  noFill();
	  stroke (150);
	  line (0,0, 30,0);
	  stroke (0);
	  line (0,0, 30*vx, 30*vy);
	  pop()
	}

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
