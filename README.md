[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24113034&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** email@example.com
**Name:** (Dien ten cua ban)

---

## Mo ta

Trong bai lab nay, em da xay dung mot ETL pipeline don gian de doc du lieu tu file JSON, loai bo cac ban ghi khong hop le, ap dung he so giam gia 10% va luu ket qua ra file CSV. Em da them thong bao logging de hien thi so ban ghi hop le va so ban ghi bi loai, cung nhu them cot `processed_at` de quan sat thoi diem xu ly.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)

Su dung `agent_simulation.py` de so sanh ket qua voi du lieu sach va du lieu rac. File `experiment_report.md` luu lai nhan xet va ket luan cua em.

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

Pipeline da xu ly 3 ban ghi hop le va loai bo 2 ban ghi khong hop le (gia <= 0 hoac category rong). Ket qua duoc luu trong `processed_data.csv` va bao gom cot `discounted_price` va `processed_at`.
