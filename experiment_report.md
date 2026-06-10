# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** AI20K-XXXX
**Name:** (Dien ten cua ban)
**Date:** (Dien ngay thuc hien)

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Agent tra loi chinh xac va dua ra ket qua hop le. | 9 | Du lieu sach, khong co gia tri sai, nen ket qua rat tot. |
| Garbage Data (`garbage_data.csv`) | Agent tra loi khong chinh xac va co nhieu sai sot. | 4 | Du lieu bi rac, co gia tri am va category rong, lam giam hieu qua. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Khi dung Garbage Data, agent bi anh huong boi chat luong du lieu dau vao. Du lieu co cac ban ghi gia tri am, category rong hoac du lieu bi thieu, lam cho mo hinh ra quyet dinh sai va khong duoc huan luyen de xu ly truong hop nay. Du lieu rac co the lam xuat hien duplicates, sai kieu du lieu, outliers va null values, lam giam do tin cay va lam rong mo hinh. Agent co xu huong dua ra du doan sai vi cac ky hieu duoc dua vao la khong-hop-le va thuat toan khong the phan biet thong tin hop le voi thong tin khong hop le.

Trong vi du nay, file `garbage_data.csv` co the chua cac hang co gia <= 0 va category trong, nhung neu pipeline khong validate du lieu, agent se tiep tuc xu ly nhung ban ghi nay va ra ket qua sai. Do do, viec lam sach du lieu truoc khi phan tich la buoc can thiet de coket qua tot hon. 

Nguoi thuc hien can chu y nhung loi sau:
- Gia am hoac bang 0 khong hop le cho san pham.
- Category rong lam cho viec nhom va phan loai san pham sai.
- Du lieu khong day du va co null values lam mo hinh khong du thong tin.
- Outliers va sai kieu du lieu lam lam sai so voi cac phep toan tim kiem va tong hop.

Chinh vi the, chat luong du lieu hon co the quan trong hon ca quality prompt neu prompt hoac mo hinh khong duoc dua tren du lieu sach va duoc lam sach truoc.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** Dong y. Du lieu chat luong cao la nen tang quan trong de mo hinh va agent hoat dong chinh xac. Neu du lieu dau vao bi rac, ngay ca mot prompt tot nhat cung khong the bao dam ket qua dung. Do do, can phai co quy trinh ETL va validate du lieu truoc khi su dung cho agent.
