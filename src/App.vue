<template>
  <div id="app">
    <div class="kb-wrapper">
      <div class="kb-top">
        <div class="kb-area">
          <ul>
            <li class="kb-key kb-esc kb-font">Esc</li>
            <li class="kb-key">F1</li>
            <li class="kb-key">F2</li>
            <li class="kb-key">F3</li>
            <li class="kb-key">F4</li>
            <li class="kb-key">F5</li>
            <li class="kb-key">F6</li>
            <li class="kb-key">F7</li>
            <li class="kb-key">F8</li>
            <li class="kb-key">F9</li>
            <li class="kb-key">F10</li>
            <li class="kb-key">F11</li>
            <li class="kb-key">F12</li>
          </ul>
        </div>
        <div class="kb-area">
          <ul>
            <li class="kb-key kb-font kb-lineheight">Print Screen</li>
            <li
              class="kb-key kb-font kb-lineheight"
              @click="iScroll = !iScroll"
            >Scroll Lock</li>
            <li class="kb-key kb-font kb-lineheight">Pause Break</li>
          </ul>
        </div>
        <div class="kb-area">
          <ul>
            <li :class="['kb-light' , { 'active': isNum }]"></li>
            <li :class="['kb-light' , { 'active': isCaps }]"></li>
            <li :class="['kb-light' , { 'active': iScroll }]"></li>
          </ul>
        </div>
      </div>
      <div class="kb-bottom">
        <div class="kb-area">
          <ul>
            <li class="kb-key">
              <span>~</span>
              <span>`</span>
            </li>
            <li class="kb-key">
              <span>!</span>
              <span>1</span>
            </li>
            <li class="kb-key">
              <span>@</span>
              <span>2</span>
            </li>
            <li class="kb-key">
              <span>#</span>
              <span>3</span>
            </li>
            <li class="kb-key">
              <span>$</span>
              <span>4</span>
            </li>
            <li class="kb-key">
              <span>%</span>
              <span>5</span>
            </li>
            <li class="kb-key">
              <span>^</span>
              <span>6</span>
            </li>
            <li class="kb-key">
              <span>&</span>
              <span>7</span>
            </li>
            <li class="kb-key">
              <span>*</span>
              <span>8</span>
            </li>
            <li class="kb-key">
              <span>(</span>
              <span>9</span>
            </li>
            <li class="kb-key">
              <span>)</span>
              <span>0</span>
            </li>
            <li class="kb-key">
              <span>—</span>
              <span>_</span>
            </li>
            <li class="kb-key">
              <span>+</span>
              <span>=</span>
            </li>
            <li class="kb-key kb-backspace kb-font">Backspace</li>
            <li class="kb-key kb-tab kb-font">Tab</li>
            <li class="kb-key">Q</li>
            <li class="kb-key">W</li>
            <li class="kb-key">E</li>
            <li class="kb-key">R</li>
            <li class="kb-key">T</li>
            <li class="kb-key">Y</li>
            <li class="kb-key">U</li>
            <li class="kb-key">I</li>
            <li class="kb-key">O</li>
            <li class="kb-key">P</li>
            <li class="kb-key">
              <span>{</span>
              <span>[</span>
            </li>
            <li class="kb-key">
              <span>}</span>
              <span>]</span>
            </li>
            <li class="kb-key kb-line">
              <span>|</span>
              <span>\</span>
            </li>
            <li
              class="kb-key kb-capslock kb-font"
              @click="isCaps = !isCaps"
            >Caps Lock</li>
            <li class="kb-key">A</li>
            <li class="kb-key">S</li>
            <li class="kb-key">D</li>
            <li class="kb-key kb-f">F</li>
            <li class="kb-key">G</li>
            <li class="kb-key">H</li>
            <li class="kb-key kb-j">J</li>
            <li class="kb-key">K</li>
            <li class="kb-key">L</li>
            <li class="kb-key">
              <span>:</span>
              <span>;</span>
            </li>
            <li class="kb-key">
              <span>"</span>
              <span>'</span>
            </li>
            <li class="kb-key kb-enter kb-font">Enter</li>
            <li class="kb-key kb-shift kb-font">Shift</li>
            <li class="kb-key">Z</li>
            <li class="kb-key">X</li>
            <li class="kb-key">C</li>
            <li class="kb-key">V</li>
            <li class="kb-key">B</li>
            <li class="kb-key">N</li>
            <li class="kb-key">M</li>
            <li class="kb-key">
              <span>&lt;</span>
              <span>,</span>
            </li>
            <li class="kb-key">
              <span>&gt;</span>
              <span>.</span>
            </li>
            <li class="kb-key">
              <span>?</span>
              <span>/</span>
            </li>
            <li class="kb-key kb-shift2 kb-font">Shift</li>
            <li class="kb-key kb-ctrl kb-font">Ctrl</li>
            <li class="kb-key"><i class="icon-windows"></i></li>
            <li class="kb-key kb-font">Alt</li>
            <li class="kb-key kb-space kb-font">Space</li>
            <li class="kb-key kb-font">Alt</li>
            <li class="kb-key"><i class="icon-windows"></i></li>
            <li class="kb-key"><i class="icon-file-text"></i></li>
            <li class="kb-key kb-ctrl kb-font">Ctrl</li>
          </ul>
        </div>
        <div class="kb-area">
          <ul>
            <li class="kb-key kb-font">Insert</li>
            <li class="kb-key kb-font">Home</li>
            <li class="kb-key kb-font kb-lineheight">Page Up</li>
            <li class="kb-key kb-font">Delete</li>
            <li class="kb-key kb-font">End</li>
            <li class="kb-key kb-font kb-lineheight">Page Down</li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li class="kb-key"><i class="icon-up"></i></li>
            <li></li>
            <li class="kb-key"><i class="icon-caret-left"></i></li>
            <li class="kb-key"><i class="icon-down"></i></li>
            <li class="kb-key"><i class="icon-caret-right"></i></li>
          </ul>
        </div>
        <div class="kb-area">
          <ul>
            <li
              class="kb-key kb-font kb-lineheight"
              @click="isNum = !isNum"
            >Num Lock</li>
            <li class="kb-key">/</li>
            <li class="kb-key">*</li>
            <li class="kb-key">-</li>
            <li class="kb-key">7</li>
            <li class="kb-key">8</li>
            <li class="kb-key">9</li>
            <li class="kb-key">+</li>
            <li class="kb-key">4</li>
            <li class="kb-key">5</li>
            <li class="kb-key">6</li>
            <li class="kb-key">1</li>
            <li class="kb-key">2</li>
            <li class="kb-key">3</li>
            <li class="kb-key kb-font">Enter</li>
            <li class="kb-key">0</li>
            <li class="kb-key">.</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      iScroll: false,
      isNum: false,
      isCaps: false
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

ul {
  list-style: none;
}

.kb-wrapper {
  width: 1460px;
  height: 410px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border-radius: 10px 10px 5px 5px;
  padding: 12px;
  margin-top: 200px;
  box-shadow: 1px 0px 12px rgba(0, 0, 0, 0.5);
}

.kb-bottom,
.kb-top {
  width: 100%;
  display: flex;
  flex-direction: row;
}

.kb-top {
  height: 78px;
}

.kb-area {
  margin: 0 8px;
  padding: 16px;
}

.kb-key {
  height: 50px;
  width: 50px;
  grid-column: span 1;
  background: #fff;
  border-radius: 6px;
  box-shadow: 3px 3px 9px #828282, -3px -3px 9px #ffffff;
  cursor: pointer;
  text-align: center;
  line-height: 50px;
  transition: all 0.2s ease;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}

.kb-key:active {
  box-shadow: 1px 1px 3px #bebebe, -1px -1px 3px #ffffff;
}

.kb-key span {
  height: 25px;
  line-height: 25px;
}

.kb-light {
  height: 3px;
  width: 8px;
}

.kb-light::before {
  content: "";
  display: block;
  height: 3px;
  width: 16px;
  border-radius: 2px;
  background-color: #888800;
  transition: all 0.4s ease;
}

.kb-light.active::before {
  background-color: #99dd00;
}

.kb-light::after {
  content: "";
  display: block;
  height: 14px;
  width: 14px;
  font-size: 12px;
  text-align: center;
  line-height: 1;
  border: 1px solid #e0e0e0;
  margin-top: 4px;
  color: #e0e0e0;
}

.kb-light:nth-child(1)::after {
  content: "1";
}

.kb-light:nth-child(2)::after {
  content: "A";
}

.kb-light:nth-child(3)::after {
  content: "\e9c7";
  font-family: 'icomoon' !important;
}

/* row-gap: 8px; column-gap: 8px; 简写： gap: 8px 8px; => gap:8px;*/
.kb-area ul {
  display: grid;
  justify-items: center;
  align-items: center;
  gap: 8px;
}

/* 第一块区域 */
.kb-top .kb-area:nth-child(1) ul,
.kb-bottom .kb-area:nth-child(1) ul {
  grid-template-columns: repeat(60, 12.5px);
  grid-template-rows: repeat(5, 50px);
  column-gap: 3px;
}

.kb-top .kb-area:nth-child(1) .kb-key,
.kb-bottom .kb-area:nth-child(1) .kb-key {
  grid-column: span 4;
}

.kb-top .kb-area:nth-child(1) .kb-esc {
  grid-column: span 12;
  width: 72px;
}

.kb-bottom .kb-area:nth-child(1) .kb-backspace {
  grid-column: span 8;
  width: 118px;
}

.kb-bottom .kb-area:nth-child(1) .kb-tab,
.kb-bottom .kb-area:nth-child(1) .kb-line,
.kb-bottom .kb-area:nth-child(1) .kb-ctrl {
  grid-column: span 6;
  width: 87px;
}

.kb-bottom .kb-area:nth-child(1) .kb-capslock {
  grid-column: span 7;
  width: 102.5px;
}

.kb-bottom .kb-area:nth-child(1) .kb-enter,
.kb-bottom .kb-area:nth-child(1) .kb-shift {
  grid-column: span 9;
  width: 133.5px;
}

.kb-bottom .kb-area:nth-child(1) .kb-shift2 {
  grid-column: span 11;
  width: 164.5px;
}

.kb-bottom .kb-area:nth-child(1) .kb-space {
  grid-column: span 28;
  width: 413px;
}

.kb-f,
.kb-j {
  position: relative;
}

.kb-f::after,
.kb-j::after {
  content: "";
  position: absolute;
  height: 2px;
  width: 8px;
  bottom: 6px;
  left: 50%;
  transform: translateX(-50%);
  background-color: #f0f0f0;
}

.kb-font {
  font-size: 14px;
}

.kb-lineheight {
  line-height: 22px;
}

/* 第二块区域 */
.kb-top .kb-area:nth-child(2) ul,
.kb-bottom .kb-area:nth-child(2) ul {
  grid-template-columns: repeat(3, 50px);
  grid-template-rows: repeat(5, 50px);
}

.kb-bottom .kb-area:nth-child(3) {
  width: 230px;
  height: 290px;
}

/* 第三块区域 */
.kb-top .kb-area:nth-child(3) ul {
  margin-top: 12px;
  grid-template-columns: repeat(3, 50px);
  box-shadow: inset 1px 1px 5px rgba(0, 0, 0, 0.1);
}

.kb-bottom .kb-area:nth-child(3) ul {
  grid-template-columns: repeat(4, 50px);
  grid-template-rows: repeat(5, 50px);
}

.kb-bottom .kb-area:nth-child(3) .kb-key:nth-child(8) {
  /* grid-row-start: 2;
  grid-row-end: 4;
  grid-column-start: 4;
  grid-column-end: 5; 简写方式如下*/
  grid-row: 2 / 4;
  grid-column: 4 / 5;
  height: 108px;
}

.kb-bottom .kb-area:nth-child(3) .kb-key:nth-child(15) {
  grid-row: 4 / 6;
  grid-column: 4 / 5;
  height: 108px;
}

.kb-bottom .kb-area:nth-child(3) .kb-key:nth-child(16) {
  grid-row: 5 / 6;
  grid-column: 1 / 3;
  width: 108px;
}
</style>
