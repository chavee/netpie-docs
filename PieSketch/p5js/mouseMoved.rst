.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

mouseMoved()
============

ฟังก์ชัน mouseMoved () เรียกว่าทุกครั้งที่เมาส์เคลื่อนที่และไม่ได้กดปุ่มเมาส์ 
เบราว์เซอร์อาจมีพฤติกรรมเริ่มต้นแตกต่างกันไปตามเหตุการณ์ต่างๆของเมาส์ หากต้องการป้องกันไม่ให้เกิดการทำงานดีฟอลต์สำหรับเหตุการณ์นี้ให้เพิ่ม "return false" ที่ด้านท้ายสุดของเมธอด

.. The mouseMoved() function is called every time the mouse moves and a mouse
.. button is not pressed.
.. 
.. Browsers may have different default
.. behaviors attached to various mouse events. To prevent any default
.. behavior for this event, add "return false" to the end of the method.

**รูปแบบการใช้งาน**

mouseMoved ( )

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	// Move the mouse across the page
	// to change its value
	
	var value = 0;
	function draw() {
	  fill(value);
	  rect(25, 25, 50, 50);
	}
	function mouseMoved() {
	  value = value + 5;
	  if (value > 255) {
	    value = 0;
	  }
	}

	</script>

	<br><br>

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	
	function mouseMoved() {
	  ellipse(mouseX, mouseY, 5, 5);
	  // prevent default
	  return false;
	}

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
