---
layout: page
title: Tips & Strick
permalink: /tips/
---

### More Information

git commands

# git diff [branch to compare] :: Exp: bạn ở nhánh b muốn xem vs nhánh dev đã thay đổi những gì.

=> git diff dev

# touch config.j :: create a new file by command-line.

# mv config.j config.js :: rename file

Jquery:
cách để ứng dụng ko bi crash do mạng yếu.
const initApp =()=>{
const orderBtn = document.querySelector('button');
orderBtn.addEventListener('click', clickOrder);
}

const clickOrder = () => console.log('clicked Item')

document.addEventListener('DOMContentLoaded', initApp); => đảm bảo các lệnh chỉ thực thi khi DOM đã được loaded.

# debounce(fn, delay); :: debounce => giúp ngăn chặn việc user click liên tục vào button.

Hàm nhận 2 tham số:
-tham số thứ 1, Exp: fn request xuống backend.
-tham số thứ 2, Exp: cho 2000ms => 2s, sau 2 giây fn request xuống backend mới thực hiện. nếu user click liên tục
thì tại thời điểm đó nó sẽ tính lại 2s. đến khi nào user ko click nữa và sau 2s nó sẽ thực hiện

const debounce =(fn, delay) => {
  delay = delay || 0;
  let timerId;
    console.log('timer immediate load:::', timerId);
  return () => {
    console.log('timer previous at::: ${timerId}');
      if(timerId){
        clearTimeout(timerId);
        timerId = null;
      }
      timerId = setTimeout(() =>{
        fn();
      }, delay)
  }
}
