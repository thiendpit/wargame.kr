## QR code puzzle

- Bài này điều kiện ta phải quét mã QR để lấy flag. QR code này bị sắp xếp đảo lộn, vì thế ta cần làm sao đó để có QR code ban đầu.
  Coi trong source ta thấy đoạn code

```javascript
  $(function(){ $('#join_img').attr('src',unescape('.%2f%69%6d%67%2f%71%72%2e%70%6e%67'));
  $('#join_img').jqPuzzle({rows:6,cols:6,shuffle:true,numbers:false,control:false,style:{overlap:false}});
  hide_pz();});
 function hide_pz(){
  var pz=$('#join_img div'); if(pz[pz.length-2]){$(pz[1]).remove();$(pz[pz.length-2]).remove();}else{setTimeout("hide_pz()",5);}

```

- Ta không cần quan tâm code hoạt động như thế nào, điều đập vào mắt mình đầu tiên là dòng
  $('#join_img').attr('src',unescape('.%2f%69%6d%67%2f%71%72%2e%70%6e%67');
  OK, cần đảo lộn vị trí các hình trong qr code thì cần phải có tấm hình nguồn. Dòng này là src của image. bỏ unescape.. vào console ra src
  để ảnh. Quét mã ra được kết quả.

  congratulations!!
  Flag is : 2134642a88d0687316608fa86ba92ed3d0dcfab6
