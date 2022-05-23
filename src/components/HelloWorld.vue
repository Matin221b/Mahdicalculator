<script>
export default {
   data() {
    return {
      screen: "",
      value1: Number,
      value2: Number,
      Mt: "",
    };
  },
  methods: {  // ‌تعریف عملگر‌های ریاضی 
    digit(n) {
      this.screen += n;
    },
    sum() {
      this.value1 = parseInt(this.screen, 10);
      this.Mt = "+";
      this.screen = "";
    },
    mul() {
      this.value1 = parseInt(this.screen, 10);
      this.Mt = "*";
      this.screen = "";
    },
    minus() {
      this.value1 = parseInt(this.screen, 10);
      this.Mt = "-";
      this.screen = "";
    },
    mod() {
      this.value1 = parseInt(this.screen, 10);
      this.Mt = "%";
      this.screen = "";
    },
    clear() {
      this.screen = "";
    },
    div() {
      this.value1 = parseInt(this.screen, 10);
      this.Mt = "/";
      this.screen = "";
    },
    equal() {
      switch (this.Mt) {
        case "+":
          this.value2 = parseInt(this.screen, 10);
          this.screen = this.value2 + this.value1;
          break;
        case "-":
          this.value2 = parseInt(this.screen, 10);
          this.screen = this.value1 - this.value2;
          break;
        case "*":
          this.value2 = parseInt(this.screen, 10);
          this.screen = this.value1 * this.value2;
          break;
        case "%":
          this.value2 = parseInt(this.screen, 10);
          this.screen = this.value1 % this.value2;
          break;
        case "/":
          this.value2 = parseInt(this.screen, 10);
          this.screen = this.value1 / this.value2;
          break;
        default:
          break;
      }
    },
  }
};
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
        <td colspan="2"><button @click="clear" id="clear">C</button></td>    <!--دکمه‌ی پاک کردن صفحه نمایش-->
        <td><button @click="mod" id="mod">%</button></td>   <!--دکمه‌ی درصد-->
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

<!--تغییرات استایل ماشین حساب-->
<style>
#calculator {
  text-align: center;
  margin: auto
}
#show {
padding: 5px;
font-weight: bold;
text-align: right
}
#equal {
  color: white;
  background-color: black ;
  border: 2px solid black;
  width: calc(100%);
  padding: 11.5px 0;
}
#digit{
  font: message-box;
  color: black;
  background-color:#DFFF00;
  border: 2px solid rgb(0, 0, 0);
  width: calc(100%);
  padding: 10px;
}
#sum {
  color: white;
  background-color: black ;
  border: 2px solid black;
  width: calc(100%);
  height: calc(88px);
  padding: 11.5px
}
#minus {
  color: white;
  background-color: black ;
  border: 2px solid black;
  width: calc(100%);
  padding: 11.5px
}
#mul {
  color: white;
  background-color: black ;
  border: 2px solid black;
  width: calc(100%);
  padding: 11.5px
}
#clear {
  color: white;
  background-color: black ;
  border: 2px solid black;
  width: calc(100%);
  padding: 11.5px
}
#div {
  color: white;
  background-color: black ;
  border: 2px solid black;
  width: calc(100%);
  padding: 11.5px
}
#mod {
  color: white;
  background-color: black ;
  border: 2px solid black;
  width: calc(100%);
  padding: 11.5px
}
</style>