# Code-Khao-Sat-Trang-Sinh-Vien

const target  = 'Phân vân';             // sửa chữ ở đây thay từ Phân vân thành nhãn bạn muốn click chú ý để nguyên dấu " "

const comment = 'Không ý kiến';    // sửa chữ ở đây thành nội dung muốn điền chú ý để nguyên dấu " "


const re = new RegExp(target, 'i');

// click radio đúng nhãn

for (const l of document.querySelectorAll('label.mt-radio')) {

  if (re.test(l.textContent)) {
  
    l.click();
    
  }
}

// điền vào ô "Ý kiến khác"

const ta = document.querySelector('textarea.input-ykien');

if (ta) ta.value = comment;


