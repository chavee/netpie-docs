.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

removeAttribute()
=================

ลบแอตทริบิวต์ในองค์ประกอบที่ระบุ

.. Removes an attribute on the specified element.

**รูปแบบการใช้งาน**

removeAttribute ( attr )

**พารามิเตอร์**

- ``attr``  String: แอตทริบิวต์ที่จะลบ

.. ``attr``  String: attribute to remove

**ค่าที่ส่งออกมา**

- Object,p5.Element: 

.. Object,p5.Element: 

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	var button;
	var checkbox;
	
	function setup() {
	  checkbox = createCheckbox('enable', true);
	  checkbox.changed(enableButton);
	  button = createButton('button');
	  button.position(10, 10);
	}
	
	function enableButton() {
	  if( this.checked() ) {
	    // Re-enable the button
	    button.removeAttribute('disabled');
	  } else {
	    // Disable the button
	    button.attribute('disabled','');
	  }
	}

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
