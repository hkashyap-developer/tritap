---
layout: post
title:  "Real Taste"
type: "restaurant"
date:   2021-12-24 00:01:58 +0530
categories: jekyll update
img-url: "https://drive.google.com/uc?export=view&id=1MhYwAOYGLWCJn81fRb87smAXJrDpChyP" 
shop-db: "pizza-hood"
comments: "true"
permalink: "tritap/testx01"
---

<style>

  @import url('https://fonts.googleapis.com/css2?family=Outfit:wght@100;200;300;400;500;600;700;800;900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Outfit:wght@100;200;300;400;500;600;700;800;900&display=swap');
* {
  font-family: 'Outfit', sans-serif;
  color:red; 
}
h1, h2 {
  font-family: 'Outfit', sans-serif;
}




.otrBxProduct {
  border:solid black 2px;
  padding:20px; 
  max-width:400px;
  min-width:360px;
  margin:0 auto; 
    margin-bottom:20px; 
    border-radius:4px; 


}


.container {
  
}

.prdDesc-r1 {
  display:flex; 
}
.prdDesc-r1c1 {
  flex:2;  
}
.prdDesc-r1c2 {
  flex:1;  
  display:flex; 
  align-itmes:center; 
  justify-content:center; 
}
.prdDesc-r2 {
  display:flex; 
}
.prdDesc-r2c1 {
  flex:1;  
}
.prdDesc-r2c2 {
  flex:1;  
  text-align:right; 
}
p.cstPrdDesc {
margin: 0px;
    font-size: 15px;
    margin-bottom: 12px;
    color: #5b5b5b;
    font-weight: 500;
}
.prdDesc-r1c1 h3 {
    margin-bottom: 2px;
    margin-bottom:12px;   
}
button.btnStyleCstm {
    padding: 4px 11px;
    background-color: none; //#dadada;
    border: none;
    font-size:22px; 
    font-radius:4px; 
}
span.cstmQtyPicker {
    margin: 0 12px;
    font-size: 18px;
    font-weight: 600;
}
.varBtn {
  border:0px; 
  padding:4px 8px; 
  font-size:12px;
  border-radius:20px;  
  margin-right:4px; 
}
.varBtn:hover {
  background-color: #cd9c20;
}
.shopMainFlex {
  display:flex;  
}
.shopPgR1C1, .shopPgR1C2, .shopPgR1C3 {
  flex:1; 
  padding:0px 24px; 
}
.shopChkOtBtn {
  width:100%; 
  font-size:24px; 
  display:none; 


}
.shopChkOtBtn.active { 
  display:block; 
}

</style>
 
<div class="otrMostBox">

<div class="container shopMainFlex">
<div class="shopPgR1C1">
 {% include cat-list.html %}
 {% include ad-banner1.html %}
</div>

  
<div class="shopPgR1C2">
{% for product in site.data.pizza-hood %}
<div class="otrBxProduct
  {%- assign flagVar=product.category | split: ', ' -%}
  {% for member in flagVar %}
  {{ member }} 
  {%- endfor -%}
">  

<div class="prdDesc">
  <div class="prdDesc-r1">
  <div class="prdDesc-r1c1">
  <h3>  
  {% assign flagVar=product.tags | split: ", " %}
  {% for member in flagVar %}
    {% if member == "veg" %}
    <img src="veg.png" width="16px">
    {% endif %}
    {% if member == "non-veg" %}
    <img src="non-veg.png" width="16px">
  {% endif %}
  {% endfor %}
  {{ product.name }}</h3>
  <p class="cstPrdDesc">{{ product.description }}</p>
  {% if product.category contains "cat1" %}
  <p class="cstPrdCat">{{ product.category }}</p>
  {% endif %}
  {% if product.var1-title!="" %}
    <button class="varBtn">{{ product.var1-title }}</button>
  {% endif %}
  {% if product.var2-title!="" %}
    <button class="varBtn">{{ product.var2-title }}</button>
  {% endif %}
  {% if product.var3-title!="" %}
    <button class="varBtn">{{ product.var3-title }}</button>
  {% endif %}
  </div>
  <div class="prdDesc-r1c2">
  <img src="{{ product.img-url }}" width="100%">
  </div>
</div>
<hr style="margin-top:12px; margin-bottom:8px; border-color:white; background-color:white;">
<div class="prdDesc-r2">
  <div class="prdDesc-r2c1">
    <strike style="color:#a2a2a2; font-weight:500; ">₹ {{ product.cost-price }}</strike>&nbsp;₹ {{ product.sale-price }}
  </div>
  <div class="prdDesc-r2c2">
     <div class="priceQty-r1c2">
        <button class="btnStyleCstm" onclick="dec{{ product.prod-id }}();">-</button><span id="{{ product.prod-id }}-qty" class="cstmQtyPicker {{ product2.prod-id }}qtyx3">0</span><button class="btnStyleCstm" onclick="inc{{ product.prod-id }}();">+</button>
      </div>
  </div>
</div>
  
</div>
</div>
{% endfor %}









<div id="disqus_thread"></div>
<script>
    /**
    *  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
    *  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables    */
    /*
    var disqus_config = function () {
    this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
    this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
    };
    */
    (function() { // DON'T EDIT BELOW THIS LINE
    var d = document, s = d.createElement('script');
    s.src = 'https://mihu-pb.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>










</div>

<div class="shopPgR1C3">
<style>
.invoiceCstmOtrBx {
  background-color:rgba(0,0,0,0.04);
  border-radius:8px; 
  padding-top:20px; 

  position:sticky; 
  top:80px; 
  display:none; 
}
.invoiceCstm-hdr{
  text-align:center;
  font-size:28px; 
  margin-bottom:20px; 
}
.shopChkOtBtn {
  border:none; 
    border-radius:8px; 
    padding:12px 0px; 
}
.invceItems-otrBx {
  display:flex; 
  padding:12px 20px; 
}
.invceItems-item, .invceItems-price {
  flex:1; 
}
.invceItems-price {
  text-align:right;
}
#checkOutButton:hover {
  background-color:#25D366; 
  color:white; 
}

</style>
<div class="invoiceCstmOtrBx">
<h3 class="invoiceCstm-hdr">Cart2</h3><hr>
<div class="invceItems-otrBx">
<div class="invceItems-item">


{% for product3 in site.data.pizza-hood %}

<p id="{{ product3.prod-id }}qtyx4">{{ product3.name }}</p>

    {% endfor %}



</div>
<div class="invceItems-price">
   {% for product3 in site.data.pizza-hood %}
    <p id="{{ product3.prod-id }}qtyx2">0</p>
   {% endfor %}

</div>
</div>
<button id="checkOutButton" class="shopChkOtBtn active" onclick="incX02();"><i class="fab fa-whatsapp"></i> Checkout</button>
</div>
</div>
</div>
</div>

<div>

  {% for product2 in site.data.pizza-hood %}
    
  <script>

  var qty{{ product2.prod-id }}=0;
    
  function inc{{ product2.prod-id }}() {
    alert("test");
    /* single product quantity increased */
    qty{{ product2.prod-id }}++;
    /* updating cookies */

    var counter=qty{{ product2.prod-id }};
    document.getElementById("{{ product2.prod-id }}qtyx2").innerHTML=counter;  
    document.getElementById("{{ product2.prod-id }}-qty").innerHTML="qty{{ product2.prod-id }}";
    document.getElementById("{{ product2.prod-id }}-qty").innerHTML=qty{{ product2.prod-id }};
    invoiceToggl();
      {% for product5 in site.data.pizza-hood %}
        qtyChkInc{{ product5.prod-id }}();
        qty{{ product2.prod-id }}
      {% endfor %}
      alert({{ product2.prod-id }}quantity);
    }

  function qtyChkInc{{ product2.prod-id }}() {
        var flagx{{ product2.prod-id }} = document.getElementById("{{ product2.prod-id }}-qty").innerHTML;
        if(flagx{{ product2.prod-id }}!=0) {
          $("#{{ product2.prod-id }}qtyx4").css("display", "block"); 
          $("#{{ product2.prod-id }}qtyx2").css("display", "block"); 
        }
    }



            function dec{{ product2.prod-id }}() {
              if(qty{{ product2.prod-id }}>0) {
              qty{{ product2.prod-id }}--;
              var counter=qty{{ product2.prod-id }};
            document.getElementById("{{ product2.prod-id }}qtyx2").innerHTML=counter;
            document.getElementById("{{ product2.prod-id }}-qty").innerHTML=qty{{ product2.prod-id }};
              }
      {% for product5 in site.data.pizza-hood %}
        qtyChkDec{{ product5.prod-id }}();
      {% endfor %}

        }


  function qtyChkDec{{ product2.prod-id }}() {
        var flagx{{ product2.prod-id }} = document.getElementById("{{ product2.prod-id }}-qty").innerHTML;
        if(flagx{{ product2.prod-id }}==0) {
          $("#{{ product2.prod-id }}qtyx4").css("display", "none"); 
          $("#{{ product2.prod-id }}qtyx2").css("display", "none"); 
        }
    }







      function invoiceToggl() {

      }

        
        function defOnLoad() {
                    document.getElementById("{{ product2.prod-id }}qtyx2").style.display="none";
          document.getElementById("{{ product2.prod-id }}qtyx4").style.display="none"; 
        }

 window.onload=defOnLoad();

   
      </script>
    {% endfor %}

    </div>
