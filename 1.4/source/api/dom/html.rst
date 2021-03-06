﻿.. currentmodule:: dom

html
=================================

Module
-----------------------------------------------

  :mod:`dom <dom>`


Methods
-----------------------------------------------

.. function:: html

    | String **html** ( selector )
    | 获取符合选择器的第一个元素的 innerHTML.
    
    :param string|HTMLCollection|Array<HTMLElement> selector: 字符串表示 `css3 选择器 <http://www.w3.org/TR/css3-selectors/>`_
    :returns: 符合选择器的第一个元素的 innerHTML.
    :rtype: String


    | void **html** ( selector , html[ , loadScripts] )
    | 给符合选择器的所有元素设置 innerHTML 值.
    
    :param string|HTMLCollection|Array<HTMLElement> selector: 字符串表示 `css3 选择器 <http://www.w3.org/TR/css3-selectors/>`_
    :param string html: 将要设置的 html 值
    :param boolean loadScripts: 是否执行 html 中的内嵌脚本，默认 false

	.. code-block:: javascript
	
	    var S = KISSY, DOM = S.DOM;

	    // 等价 document.createElement('div')
	    DOM.create('<div id="J_check"></div>');
	    var html = "<h3>This is the added part</h3><script>alert(1)</script>";
	    DOM.html("#J_check", html); // 不会 alert(1)
	    DOM.html("#J_check"); // => <h3>This is the added part</h3>
	    DOM.html("#J_check", html, true); // alert(1)


.. note::

    内嵌脚本指 ``<script>xx</script>`` or ``<script src='yy'></script>``