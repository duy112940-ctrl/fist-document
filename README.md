# fist-document
import random

def doan_so():
    print("--- TRÒ CHƠI ĐOÁN SỐ NGẪU NHIÊN ---")
    # Máy tính chọn 1 số từ 1 đến 100
    so_bi_mat = random.randint(1, 100)
    so_lan_doan = 0
    
    while True:
        try:
            # Nhập số từ người chơi
            doan = int(input("Nhập một số từ 1 đến 100: "))
            so_lan_doan += 1
            
            # So sánh
            if doan < so_bi_mat:
                print("Số bạn đoán NHỎ HƠN số bí mật. Thử lại nhé!")
            elif doan > so_bi_mat:
                print("Số bạn đoán LỚN HƠN số bí mật. Thử lại nhé!")
            else:
                print(f"🎉 Chúc mừng! Bạn đã tìm ra số {so_bi_mat} sau {so_lan_doan} lần đoán.")
                break
        except ValueError:
            print("Vui lòng nhập một số nguyên hợp lệ!")

if __name__ == "__main__":
    doan_so()
