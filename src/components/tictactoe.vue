<template>
  <div class="container">
    <h1 class="text-3xl my-3 text-center font-bold">TicTacToe</h1>
    <p class="turn"></p>
    <div class="flex flex-wrap w-2/3 mx-auto">
      <div class="slot py-4 font-bold text-center w-1/3 text-3xl">&nbsp;</div>
      <div
        class="
          slot
          py-4
          font-bold
          text-center
          w-1/3
          text-3xl
          border-r-4 border-l-4 border-black
        "
      >
        &nbsp;
      </div>
      <div class="slot py-4 font-bold text-center w-1/3 text-3xl">&nbsp;</div>

      <div
        class="
          slot
          py-4
          font-bold
          text-center
          w-1/3
          text-3xl
          border-t-4 border-b-4 border-black
        "
      >
        &nbsp;
      </div>
      <div
        class="
          slot
          py-4
          font-bold
          text-center
          w-1/3
          text-3xl
          border-4 border-black
        "
      >
        &nbsp;
      </div>
      <div
        class="
          slot
          py-4
          font-bold
          text-center
          w-1/3
          text-3xl
          border-t-4 border-b-4 border-black
        "
      >
        &nbsp;
      </div>

      <div class="slot py-4 font-bold text-center w-1/3 text-3xl">&nbsp;</div>
      <div
        class="
          slot
          py-4
          font-bold
          text-center
          w-1/3
          text-3xl
          border-r-4 border-l-4 border-black
        "
      >
        &nbsp;
      </div>
      <div class="slot py-4 font-bold text-center w-1/3 text-3xl">&nbsp;</div>
    </div>
  </div>
</template>

<script>
import $ from "jquery";

export default {
  name: "TicTacToe",
  mounted() {
    var x = "X";
    var o = "O";
    var turn = Math.ceil(Math.random() * 2);

    if (turn == 1) {
      $(".turn").html("Ход: " + x);
    } else {
      $(".turn").html("Ход: " + o);
    }

    $(".slot").on("click", function () {
      if ($(this).text() != x && $(this).text() != o) {
        if (turn == 1) {
          $(this).html(x);
          turn = 2;
          $(".turn").html("Ход: " + o);
          console.log("Ходит нолик");
        } else {
          $(this).html(o);
          turn = 1;
          console.log("Ходит крестик");
          $(".turn").html("Ход: " + x);
        }
      } else {
        console.log("Данный слот уже занят");
      }
    });
  },
};
</script>