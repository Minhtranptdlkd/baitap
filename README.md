# baitap
# cau1
def tinh_tien_taxi(km):
    if km <= 1:
        tien = 15000
    elif km <= 5:
        tien = 15000 + (km - 1) * 13500
    else:
        tien = 15000 + 4 * 13500 + (km - 5) * 11000

    if km > 120:
        giam_gia = 0.1 * tien
        tien -= giam_gia

    return tien
# cau2
def xep_loai_hoc_sinh(diem_trung_binh):
    if diem_trung_binh >= 9.0:
        xep_loai = "Xuất sắc"
    elif 8.0 <= diem_trung_binh < 9.0:
        xep_loai = "Giỏi"
    elif 6.5 <= diem_trung_binh < 8.0:
        xep_loai = "Khá"
    elif 5.0 <= diem_trung_binh < 6.5:
        xep_loai = "Trung bình"
    elif 3.5 <= diem_trung_binh < 5.0:
        xep_loai = "Yếu"
    else:
        xep_loai = "Kém"
    
    return xep_loai

# Nhập điểm trung bình từ bàn phím
diem_tb = float(input("Nhập điểm trung bình: "))

# Xác định và in xếp loại học sinh
xep_loai = xep_loai_hoc_sinh(diem_tb)
print(f"Xếp loại học sinh: {xep_loai}")


