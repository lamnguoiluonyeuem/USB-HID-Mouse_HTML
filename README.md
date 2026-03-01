## Parse & tính toán

- s16(lo, hi) — 2 byte → signed int16
- reports[] — parse hex → {dx, dy, btn, scroll}
- pts[] — cộng dồn delta → tọa độ tuyệt đối + speed

## Render

- toC(x, y) — tọa độ thực → pixel canvas (uniform scale, căn giữa)
- drawBackground() — xóa canvas + vẽ lưới
- render(upTo) — vẽ trail + glow + mũi tên + marker Start/End
- getColor(i) / getWidth(i) — lấy màu/độ dày theo mode hiện tại

## Màu sắc

- speedColor(speed) — chậm→xanh, nhanh→đỏ
- timeColor(i) — đầu→xanh, cuối→tím
- dirColor(dx, dy) — góc di chuyển → HSL hue

## Tương tác

- setMode(m) — đổi chế độ màu
- toggleArrows() / toggleGrid() — bật/tắt lớp hiển thị
- animateIt() — phát lại từng frame qua requestAnimationFrame
- mousemove — tìm điểm gần nhất → hiện frame info
