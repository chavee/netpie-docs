.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

mouseMoved()
============

ฟังก์ชัน. mouseMoved () เรียกว่าครั้งทุกครั้งที่เมาส์เคลื่อนที่ผ่านองค์ประกอบ สามารถใช้เพื่อแนบผู้ฟังเหตุการณ์เฉพาะบางส่วน

.. The .mouseMoved() function is called once every time a
.. mouse moves over the element. This can be used to attach an
.. element specific event listener.

**รูปแบบการใช้งาน**

mouseMoved ( fxn )

**พารามิเตอร์**

- ``fxn``  function: ฟังก์ชั่นที่จะยิงเมื่อเมาส์ถูกย้ายไปยังองค์ประกอบ

.. ``fxn``  function: function to be fired when mouse is moved over the element.

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	var cnv;
	var d = 30;
	var g;
	function setup() {
	  cnv = createCanvas(100, 100);
	  cnv.mouseMoved(changeSize); // attach listener for
	                              // activity on canvas only
	  d = 10;
	  g = 100;
	}
	
	function draw() {
	  background(g);
	  fill(200);
	  ellipse(width/2, height/2, d, d);
	}
	
	// this function fires when mouse moves anywhere on
	// page
	function mouseMoved() {
	  g = g + 5;
	  if (g > 255) {
	    g = 0;
	  }
	}
	
	// this function fires when mouse moves over canvas
	function changeSize() {
	  d = d + 2;
	  if (d > 100) {
	    d = 0;
	  }
	}

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
