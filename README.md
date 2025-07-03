# Khảo Sát Trang Sinh Viên IUH

## Mô tả
Một script JavaScript nhỏ giúp bạn tự động:
- Chọn radio theo **nhãn** bạn chỉ định.
- Điền vào ô **“Ý kiến khác”** với **nội dung** bạn muốn.

Chỉ cần chỉnh hai biến `target` và `comment` rồi chạy trong Console của trình duyệt.

---

## Nội dung script

```javascript
// ==== TÙY CHỈNH ====
const target  = 'Phân vân'; // Đổi 'Phân vân' thành nhãn radio bạn muốn chọn chú ý để nguyên dấu " "

const comment = 'Không ý kiến';// Đổi 'Không ý kiến' thành nội dung bạn muốn điền chú ý để nguyên dấu " "

const re = new RegExp(target, 'i');

// 1. Tự động click radio có nhãn khớp
for (const l of document.querySelectorAll('label.mt-radio')) {
  if (re.test(l.textContent)) {
    l.click();
  }
}

// 2. Tự động điền vào textarea nếu tồn tại
const ta = document.querySelector('textarea.input-ykien');
if (ta) ta.value = comment;
