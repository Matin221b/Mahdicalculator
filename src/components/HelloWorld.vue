<script>
</script>

<template>
  <div>
    <table id="calculator" dir="rtl">  <!--جدول-->
      <tr>
      
        <td colspan="4">
          <input v-model="screen" dir="rtl" id="show" type="number"/>   <!--صفحه نمایش-->
        </td>
      
      </tr>
      <tr>
        <td><button @click="mod" id="mod">%</button></td>   <!--دکمه‌ی درصد-->
        <td colspan="2"><button @click="clear" id="clear">C</button></td>    <!--دکمه‌ی پاک کردن صفحه نمایش-->
        <td><button @click="mul" id="mul">*</button></td>   <!--دکمه‌ی ضربدر-->
      </tr>
      <tr>
        <td><button @click="digit(9)" id="digit" class="digit">9</button></td>   <!--9دکمه‌ی عدد-->
        <td><button @click="digit(8)" id="digit" class="digit">8</button></td>   <!--8دکمه‌ی عدد-->
        <td><button @click="digit(7)" id="digit" class="digit">7</button></td>   <!--7دکمه‌ی عدد-->
        <td><button @click="div" id="div">/</button></td>   <!--دکمه‌ی تقسیم-->
      </tr>
      <tr>
        <td><button @click="digit(6)" id="digit" class="digit">6</button></td>   <!--6دکمه‌ی عدد-->
        <td><button @click="digit(5)" id="digit" class="digit">5</button></td>   <!--5دکمه‌ی عدد-->
        <td><button @click="digit(4)" id="digit" class="digit">4</button></td>   <!--4دکمه‌ی عدد-->
        <td><button @click="minus" id="minus">-</button></td>    <!--دکمه‌ی تفریق-->
      </tr>
      <tr>
        <td><button @click="digit(3)" id="digit" class="digit">3</button></td>   <!--3دکمه‌ی عدد-->
        <td><button @click="digit(2)" id="digit" class="digit">2</button></td>   <!--2دکمه‌ی عدد-->
        <td><button @click="digit(1)" id="digit" class="digit">1</button></td>   <!--1دکمه‌ی عدد-->
        <td rowspan="2" ><button @click="sum" id="sum">+</button></td>    <!--دکمه‌ی جمع-->
      </tr>
      <tr>
        <td colspan="2"><button @click="equal" id="equal">=</button></td>    <!--دکمه‌ی مساوی-->
        <td><button @click="digit(0)" id="digit" class="digit">0</button></td>   <!--0دکمه‌ی عدد-->
      </tr>
    </table>
  </div>
</template>

<style>
</style>