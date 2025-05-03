<script setup>
import { jsPDF } from "jspdf";
import autoTable from 'jspdf-autotable';
import '../assets/pdf-font/msjh'// 引入字體定義檔
const doc = new jsPDF()

doc.setFont('msjh')// 使用註冊的字體名稱


const savePdf = () =>{
  doc.setFontSize(20);
  doc.text("出餐單", 10, 10);
  doc.setFontSize(12);
  doc.text(`桌號：A3`, 10, 20);
  doc.text(`時間：2025/05/01 12:34`, 10, 30);
  doc.save('出餐單.pdf');
}
</script>

<template>
  <button @click="savePdf">儲存Pdf</button>
</template>

