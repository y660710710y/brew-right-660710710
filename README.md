# 🎓 520335 วิทยาการข้อมูลและเครื่องมือ - Project Brew-Right Template

ยินดีต้อนรับสู่ Template Repository สำหรับวิชา Data Science and Tools!

## 🚀 เริ่มต้นใช้งาน

1. คลิกปุ่ม **"Use this template"** เพื่อสร้าง repository ของคุณเอง
2. คลิก **"Create codespace on main"** เพื่อเปิดสภาพแวดล้อมการพัฒนา
3. รอให้ระบบ build environment (ครั้งแรกประมาณ 3-5 นาที)
4. เปิด terminal แล้วรันคำสั่ง: `docker-compose up -d`
5. เข้าใช้งาน MinIO Console ที่ http://localhost:9001 (username/password: minioadmin/minioadmin)

## 📚 Lab รายสัปดาห์

### พื้นฐาน (สัปดาห์ 1-5)
- **สัปดาห์ 1**: ภาพรวมโครงการและการตั้งค่า GitHub
- **สัปดาห์ 2**: เรียนรู้ Medallion Architecture และการจัดการ Docker
- **สัปดาห์ 3**: การดึงข้อมูลและการทำงานร่วมกันด้วย Git
- **สัปดาห์ 4**: การแปลงข้อมูลด้วย dbt + แนวคิด CI
- **สัปดาห์ 5**: dbt ขั้นสูง + GitHub Actions ครั้งแรก

### การวิเคราะห์ข้อมูล (สัปดาห์ 6-8)
- **สัปดาห์ 6**: การแบ่งกลุ่มลูกค้า (Customer Segmentation)
- **สัปดาห์ 7**: การพยากรณ์ยอดขาย (Time Series Forecasting)
- **สัปดาห์ 8**: Apache Iceberg และ Time Travel

### หัวข้อขั้นสูง (สัปดาห์ 10-14)
- **สัปดาห์ 10**: Computer Vision - ติดตามการใช้โต๊ะ
- **สัปดาห์ 11**: Audio Processing - วิเคราะห์เสียงเครื่องชงกาแฟ
- **สัปดาห์ 12**: LLM Integration - วิเคราะห์รีวิวลูกค้า
- **สัปดาห์ 13**: IoT Predictive Stock Management
- **สัปดาห์ 14**: Full-Stack API + CI/CD Pipeline สมบูรณ์

### Final Project (สัปดาห์ 15)

## 🛠️ เครื่องมือที่ใช้ (22 Tools)

### โครงสร้างพื้นฐาน (Infrastructure)
- Docker, Docker Compose, GitHub Codespaces, GitHub Actions

### การจัดเก็บข้อมูล (Data Storage)
- MinIO (S3-compatible), DuckDB, Apache Iceberg, Parquet

### การประมวลผลข้อมูล (Data Processing)
- dbt, Python, SQL, Pandas, requests, BeautifulSoup

### Machine Learning
- Scikit-learn, TensorFlow, Prophet, XGBoost, OpenAI API, LangChain, YOLO

### เครื่องมือเฉพาะทาง
- OpenCV (Computer Vision), Librosa (Audio), MQTT (IoT), FastAPI, Streamlit

## 📝 การประเมินผล

| รายการ | คะแนน | สัปดาห์ |
|--------|-------|---------|
| Quiz 1: Docker & Data Ingestion | 5% | สัปดาห์ 4 |
| Quiz 2: Transformations & ML | 10% | สัปดาห์ 7 |
| สอบกลางภาค | 20% | สัปดาห์ 9 |
| Assignment 1: Complete Pipeline | 10% | สัปดาห์ 5 |
| Assignment 2: Advanced Analytics | 10% | สัปดาห์ 11 |
| Final Project | 25% | สัปดาห์ 15 |
| Lab | 20% | 14 สัปดาห์ |
| **รวม** | **100%** | |

## 📁 โครงสร้างโฟลเดอร์

```
brew-right-project/
├── .devcontainer/       # การตั้งค่า Codespaces
├── config/              # ไฟล์ config ต่างๆ
│   └── mosquitto/       # MQTT broker config
├── data/                # ข้อมูล (git ignore)
│   ├── minio/           # MinIO storage
│   └── mosquitto/       # MQTT data
├── dbt_project/         # dbt models และ tests
├── notebooks/           # Jupyter notebooks รายสัปดาห์
├── src/                 # Python source code
├── tests/               # Unit tests
├── docker-compose.yml   # Services configuration
├── requirements.txt     # Python dependencies
└── README.md            # ไฟล์นี้

```

## 🚨 ข้อควรระวัง

1. **อย่า commit ข้อมูลจริง** - ตรวจสอบ .gitignore ก่อน commit
2. **อย่าแชร์ credentials** - ใช้ environment variables
3. **Push ขึ้น Remote บ่อยๆ** - โดยเฉพาะก่อนทำ assignment ใหญ่
4. **ทดสอบใน branch แยก** - อย่าทำงานใน main branch โดยตรง

## 💡 Tips & Tricks

### การใช้ Git อย่างมีประสิทธิภาพ
```bash
# สร้าง branch ใหม่สำหรับแต่ละ feature
git checkout -b week03-data-ingestion

# commit บ่อยๆ พร้อม message ที่ชัดเจน
git add .
git commit -m "เพิ่ม script สำหรับดึงข้อมูลจาก API"

# push และสร้าง Pull Request
git push origin week03-data-ingestion
```

### การจัดการ Docker
```bash
# ดู services ที่กำลังรัน
docker-compose ps

# ดู logs ของ service
docker-compose logs minio

# หยุด services ทั้งหมด
docker-compose down

# ลบข้อมูลทั้งหมดและเริ่มใหม่
docker-compose down -v
```

### การเข้าถึง Services

| Service | URL | Username | Password |
|---------|-----|----------|----------|
| MinIO Console | http://localhost:9001 | minioadmin | minioadmin |
| MQTT Broker | http://localhost:1883 | - | - |
| FastAPI Docs | http://localhost:8000/docs | - | - |
| Streamlit App | http://localhost:8501 | - | - |
| dbt Docs | http://localhost:8080 | - | - |

## 🔗 แหล่งข้อมูลเพิ่มเติม

- **เอกสารประกอบการสอน**: [จะแชร์ link ภายหลัง]
- **dbt Documentation**: https://docs.getdbt.com
- **MinIO Documentation**: https://min.io/docs/
- **GitHub Actions**: https://docs.github.com/actions
- **Python Official**: https://docs.python.org/3/

## 🆘 ต้องการความช่วยเหลือ?

1. **ถาม TA** ในช่วง Lab
2. **ติดต่ออาจารย์** ในชั่วโมง Office Hours

## 👥 ผู้สอน
- **ผศ.ดร.ณัฐโชติ พรหมฤทธิ์**
- **อ.ดร.สัจจาภรณ์ ไวจรรยา**

---

### 🎯 Project Brew-Right: คาเฟ่อัจฉริยะ

ตลอดภาคเรียนนี้ เราจะสร้างระบบวิเคราะห์ข้อมูลสำหรับร้านกาแฟตั้งแต่เริ่มต้นจนเป็นระบบที่สมบูรณ์ พร้อมด้วย:

- 📊 **Data Pipeline** แบบ Medallion Architecture
- 🤖 **Machine Learning** สำหรับการพยากรณ์และแบ่งกลุ่มลูกค้า
- 👁️ **Computer Vision** สำหรับติดตามการใช้โต๊ะ
- 🎵 **Audio Analytics** สำหรับตรวจจับเครื่องเสีย
- 💬 **LLM Integration** สำหรับวิเคราะห์รีวิว
- 📡 **IoT Sensors** สำหรับจัดการ Stock
- 🚀 **CI/CD Pipeline** แบบมืออาชีพ

เตรียมตัวให้พร้อมสำหรับการเดินทางสู่โลกของ Data Science! ☕🚀

---

*Last updated: Jul 2025*
