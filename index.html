<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>ระบบจัดการเวลาเรียนและตรวจสอบพฤติกรรม นตท.</title>
    <style>
        /* --- 1. โค้ดพื้นหลังเดิมของคุณ --- */
        body {
            background: linear-gradient(-45deg, #ff4d4d, #1e3c72, #00a8ff, #800000);
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
            font-family: 'Sarabun', sans-serif;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .sub-btn {
            padding: 10px 20px;
            margin: 6px;
            font-size: 15px;
            background-color: #ffffff;
            color: #1e3c72;
            border: 2px solid #1e3c72;
            border-radius: 8px;
            cursor: pointer;
            font-weight: bold;
            transition: 0.2s;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .sub-btn:hover {
            background-color: #1e3c72;
            color: white;
            transform: translateY(-2px);
        }

        /* --- 2. สไตล์ระบบควบคุมหน้าจอ --- */
        .hidden {  
            display: none !important; 
        }

        .container {
            background: rgba(255, 255, 255, 0.95);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.3);
            width: 100%;
            max-width: 450px;
            color: #333;
        }

        h2, h3 { 
            text-align: center; 
            margin-bottom: 15px; 
            color: #1e3c72; 
        }

        .form-group { 
            margin-bottom: 15px; 
        }

        label { 
            display: block; 
            margin-bottom: 5px; 
            font-weight: bold; 
            font-size: 14px;
        }

        input[type="text"], input[type="password"], input[type="date"] {
            width: 100%; 
            padding: 12px; 
            border: 1px solid #ccc; 
            border-radius: 6px; 
            font-size: 15px;
            box-sizing: border-box;
            text-align: center;
        }

        .submit-btn {
            width: 100%; 
            padding: 12px; 
            background: #0072ff; 
            color: white; 
            border: none; 
            border-radius: 6px; 
            font-size: 16px; 
            cursor: pointer; 
            font-weight: bold;
        }
        .submit-btn:hover { background: #0055cc; }

        .user-info {
            background: rgba(255, 255, 255, 0.9);
            padding: 10px 20px;
            border-radius: 8px;
            margin-bottom: 20px;
            font-size: 14px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            width: 100%;
            max-width: 950px;
            box-sizing: border-box;
        }

        .logout-btn { 
            background: #ff4d4d; 
            padding: 6px 12px; 
            font-size: 12px; 
            color: white; 
            border: none; 
            border-radius: 4px; 
            cursor: pointer; 
            font-weight: bold;
        }
        .logout-btn:hover { background: #cc0000; }

        #dashboardSection {
            width: 100%;
            max-width: 1000px;
        }

        .dashboard-content {
            background: rgba(255, 255, 255, 0.95);
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 6px 15px rgba(0,0,0,0.2);
            text-align: center;
        }
    </style>
</head>
<body>

    <!-- ================= หน้าที่ 1: ระบบล็อกอินรายบุคคล ================= -->
    <div id="loginSection" class="container">
        <h2>ระบบตรวจสอบพฤติกรรม นตท..</h2>
        <h3>ชั้นปีที่ 2 ตอน 21</h3>
        <form id="loginForm" onsubmit="handleLogin(event)">
            <div class="form-group">
                <label for="username">ชื่อผู้ใช้งาน / เลขประจำตัว</label>
                <input type="text" id="username" placeholder="กรอกชื่อผู้ใช้ หรือเลขประจำตัว" required>
            </div>
            <div class="form-group">
                <label for="password">รหัสผ่าน</label>
                <input type="password" id="password" placeholder="กรอกรหัสผ่าน" required>
            </div>
            <button type="submit" class="submit-btn">เข้าสู่ระบบ</button>
        </form>
    </div>


    <!-- ================= หน้าที่ 2: ระบบตรวจบันทึกหลัก ================= -->
    <div id="dashboardSection" class="hidden">
        
        <div class="user-info">
            <span>ผู้ใช้งานปัจจุบัน: <strong id="displayUser">อาจารย์ผู้ควบคุม</strong></span>
            <button class="logout-btn" onclick="handleLogout()">ออกจากระบบ</button>
        </div>

        <!-- โลโก้หน่วยงานของคุณ -->
        <div style="position: fixed; top: 20px; right: 20px; z-index: 1000;">
            <img src="IMG_0746.PNG" alt="Logo" style="width: 130px; height: auto; object-fit: contain; mix-blend-mode: screen;"> 
        </div>

        <h1 style="text-align: center; color: white; margin-bottom: 20px;">ระบบจัดการเวลาเรียนและตรวจสอบพฤติกรรมนตท.ชั้นปีที่ 2 ตอน 21</h1>
        
        <!-- กล่องเลือกวันที่จากปฏิทิน -->
        <div class="dashboard-content" style="max-width: 500px; margin: 0 auto 20px auto;">
            <div class="form-group" style="margin-bottom: 0;">
                <label for="checkDate" style="font-size: 16px; margin-bottom: 8px;">📅 กรุณาเลือกวันที่ต้องการตรวจสอบ:</label>
                <input type="date" id="checkDate" onchange="onDateChange()">
            </div>
        </div>

        <!-- แผงแสดงคาบเรียน (จะถูกเปิดขึ้นมาอัตโนมัติหลังจากเลือกวันที่) -->
        <div id="subjectsSection" class="dashboard-content hidden" style="margin-bottom: 25px;">
            <h3 id="day-label" style="color: #1e3c72; margin-bottom: 15px;"></h3>
            
            <div id="monday-subjects" style="display: none;">
                <button class="sub-btn" onclick="showAttendance('วันจันทร์ คาบ 1: ฟิสิกส์')">คาบ 1: ฟิสิกส์</button>
                <button class="sub-btn" onclick="showAttendance('วันจันทร์ คาบ 2: คณิตศาสตร์เพิ่มเติม')">คาบ 2: คณิตศาสตร์เพิ่มเติม</button>
                <button class="sub-btn" onclick="showAttendance('วันจันทร์ คาบ 3-4: เคมี')">คาบ 3-4: เคมี</button>
                <button class="sub-btn" onclick="showAttendance('วันจันทร์ คาบ 5: เศรษฐศาสตร์')">คาบ 5: เศรษฐศาสตร์</button>
                <button class="sub-btn" onclick="showAttendance('วันจันทร์ คาบ 6: Lab')">คาบ 6: Lab</button>
                <button class="sub-btn" onclick="showAttendance('วันจันทร์ คาบ 7-8: กิจกรรมชมรม')">คาบ 7-8: กิจกรรมชมรม</button>
            </div>
            <div id="tuesday-subjects" style="display: none;">
                <button class="sub-btn" onclick="showAttendance('วันอังคาร คาบ 2: คณิตพื้นฐาน')">คาบ 2: คณิตพื้นฐาน</button>
                <button class="sub-btn" onclick="showAttendance('วันอังคาร คาบ 2: ประวัติศาสตร์')">คาบ 2: ประวัติศาสตร์</button>
                <button class="sub-btn" onclick="showAttendance('วันอังคาร คาบ 3: คณิตเพิ่มเติม')">คาบ 3: คณิตเพิ่มเติม</button>
                <button class="sub-btn" onclick="showAttendance('วันอังคาร คาบ 4: Upbeat')">คาบ 4: Upbeat</button>
                <button class="sub-btn" onclick="showAttendance('วันอังคาร คาบ 5: เคมี')">คาบ 5: เคมี</button>
                <button class="sub-btn" onclick="showAttendance('วันอังคาร คาบ 6-7: ฟิสิกส์')">คาบ 6-7: ฟิสิกส์</button>
            </div>
            <div id="wednesday-subjects" style="display: none;">
                <button class="sub-btn" onclick="showAttendance('วันพุธ คาบ 1: การเขียน')">คาบ 1: การเขียน</button>
                <button class="sub-btn" onclick="showAttendance('วันพุธ คาบ 2: ฟิสิกส์')">คาบ 2: ฟิสิกส์</button>
                <button class="sub-btn" onclick="showAttendance('วันพุธ คาบ 3: คณิตศาสตร์เพิ่มเติม')">คาบ 3: คณิตศาสตร์เพิ่มเติม</button>
                <button class="sub-btn" onclick="showAttendance('วันพุธ คาบ 4: ภาษาไทย')">คาบ 4: ภาษาไทย</button>
                <button class="sub-btn" onclick="showAttendance('วันพุธ คาบ 5: เศรษฐศาสตร์')">คาบ 5: เศรษฐศาสตร์</button>
                <button class="sub-btn" onclick="showAttendance('วันพุธ คาบ 6: แนะแนว/ห้องสมุด')">คาบ 6: แนะแนว/ห้องสมุด</button>
                <button class="sub-btn" onclick="showAttendance('วันพุธ คาบ 7: ALC')">คาบ 7: ALC</button>
            </div>
            <div id="thursday-subjects" style="display: none;">
                <button class="sub-btn" onclick="showAttendance('วันพฤหัสบดี คาบ 1: การอบรมทางทหาร(กรม.นร.ฯ)')">คาบ 1: การอบรมทางทหาร(กรม.นร.ฯ)</button>
                <button class="sub-btn" onclick="showAttendance('วันพฤหัสบดี คาบ 2: วิทยาศาสตร์การกีฬา')">คาบ 2: วิทยาศาสตร์การกีฬา</button>
                <button class="sub-btn" onclick="showAttendance('วันพฤหัสบดี คาบ 3: ฟุตบอล')">คาบ 3: ฟุตบอล</button>
                <button class="sub-btn" onclick="showAttendance('วันพฤหัสบดี คาบ 4: สุขศึกษา')">คาบ 4: สุขศึกษา</button>
                <button class="sub-btn" onclick="showAttendance('วันพฤหัสบดี คาบ 5-7: วิชาทหาร-ตำรวจ/กิจกรรมทางทหาร')">คาบ 5-7: วิชาทหาร-ตำรวจ/กิจกรรมทางทหาร</button>
            </div>
            <div id="friday-subjects" style="display: none;">
                <button class="sub-btn" onclick="showAttendance('วันศุกร์ คาบ 1: ภาษาจีน')">คาบ 1: ภาษาจีน</button>
                <button class="sub-btn" onclick="showAttendance('วันศุกร์ คาบ 2: ภาษาไทย')">คาบ 2: ภาษาไทย</button>
                <button class="sub-btn" onclick="showAttendance('วันศุกร์ คาบ 3: Conversation')">คาบ 3: Conversation</button>
                <button class="sub-btn" onclick="showAttendance('วันศุกร์ คาบ 4: คณิตศาสตร์พื้นฐาน')">คาบ 4: คณิตศาสตร์พื้นฐาน</button>
                <button class="sub-btn" onclick="showAttendance('วันศุกร์ คาบ 5: ทัศนศิลป์')">คาบ 5: ทัศนศิลป์</button>
                <button class="sub-btn" onclick="showAttendance('วันศุกร์ คาบ 5-6: คอมพิวเตอร์')">คาบ 5-6: คอมพิวเตอร์</button>
            </div>
            <div id="weekend-message" style="display: none; color: #ff4d4d; font-weight: bold; padding: 15px;">
                ⚠️ วันที่เลือกเป็นวันหยุดเสาร์-อาทิตย์ ไม่มีตารางเรียนในระบบ
            </div>
        </div>

        <!-- กล่องตารางตรวจสอบพฤติกรรมของคุณ (จะแสดงผลเมื่อกดเลือกคาบเรียน) -->
        <div id="attendance-box" style="display: none; background: rgba(255, 255, 255, 0.95); padding: 20px; border-radius: 15px; max-width: 950px; margin: 0 auto; box-shadow: 0 4px 15px rgba(0,0,0,0.2);">
            
            <h2 id="current-subject" style="color: #2c3e50; text-align: center; margin-top: 0;"></h2>
            <p id="current-date-display" style="text-align: center; color: #0044cc; font-weight: bold; margin-bottom: 10px; font-size: 16px;"></p>
            
            <div style="text-align: center; margin-bottom: 20px;">
                <img src="IMG_1181.jpg.JPG" alt="ตารางเรียน นตท. ชั้นปีที่ ๒ ตอน ๒๑" width="400" style="border-radius: 8px;">
            </div>

            <p style="text-align: center; font-weight: bold;">เวลา มาเรียน-ขาดเรียน ของ นตท.</p>

            <table style="width: 100%; border-collapse: collapse; background: white;">
                <thead>
                    <tr style="background-color: #1e3c72; color: white;">
                        <th style="padding: 10px; border: 1px solid #ddd;">ลำดับ</th>
                        <th style="padding: 10px; border: 1px solid #ddd; text-align: left;">ชื่อ-นามสกุล</th>
                        <th style="padding: 10px; border: 1px solid #ddd;">มาเรียน</th>
                        <th style="padding: 10px; border: 1px solid #ddd;">ลา</th>
                        <th style="padding: 10px; border: 1px solid #ddd;">ขาดเรียน</th>
                        <th style="padding: 10px; border: 1px solid #ddd; color: #d97706;">หลับ</th>
                        <th style="padding: 10px; border: 1px solid #ddd; color: #dc2626;">โนหนังสือ</th>
                        <th style="padding: 10px; border: 1px solid #ddd; color: #059669;">ขาดความรุกรบ</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">1</td>
                        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">นตท.ปรเมศวร์ จงชมผา</td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">2</td>
                        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">นตท. ภานุพงศ์ พุทสุข</td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                    </tr>
                    <tr>
                        <td style="padding: 10px; border: 1px solid #ddd; text-align: center;">3</td>
                        <td style="padding: 10px; border: 1px solid #ddd; text-align: left;">นตท.ภูพริษฐ์ แสงมรกต</td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                        <td style="text-align: center; border: 1px solid #ddd;"><input type="checkbox"></td>
                    </tr>
                </tbody>
            </table>
            
            <button class="submit-btn" style="margin-top: 25px; background-color: #22c55e;" onclick="alert('บันทึกข้อมูลประจำวันนี้สำเร็จ!')">บันทึกข้อมูลสำเร็จ</button>
        </div>

    </div>

    <!-- ================= 3. ส่วนควบคุม JavaScript ================= -->
    <script>
        // ฟังก์ชันระบบล็อกอิน
        function handleLogin(event) {
            event.preventDefault();
            const username = document.getElementById('username').value;
            
            document.getElementById('loginSection').classList.add('hidden');
            document.getElementById('dashboardSection').classList.remove('hidden');
            document.getElementById('displayUser').innerText = username;

            // ตั้งค่าวันที่ปัจจุบันในปฏิทินเมื่อล็อกอินสำเร็จ
            const today = new Date().toISOString().split('T')[0];
            document.getElementById('checkDate').value = today;
            onDateChange();
        }

        // ฟังก์ชันออกจากระบบ
        function handleLogout() {
            document.getElementById('dashboardSection').classList.add('hidden');
            document.getElementById('loginSection').classList.remove('hidden');
            document.getElementById('username').value = '';
            document.getElementById('password').value = '';
            
            // ซ่อนพื้นที่ทำงานเก่าทั้งหมด
            document.getElementById('subjectsSection').classList.add('hidden');
            document.getElementById('attendance-box').style.display = 'none';
        }

        // ฟังก์ชันทำงานอัตโนมัติเมื่อมีการเลือกหรือเปลี่ยนวันที่ในปฏิทิน
        function onDateChange() {
            const selectedDate = document.getElementById('checkDate').value;
            if(!selectedDate) return;

            // เคลียร์ตารางเช็กชื่อของเก่าออกก่อน
            document.getElementById('attendance-box').style.display = 'none';

            // ดึงค่าวันในสัปดาห์ (0 = อาทิตย์, 1 = จันทร์, ..., 6 = เสาร์)
            const dateObj = new Date(selectedDate);
            const dayOfWeek = dateObj.getDay();

            // จัดรูปแบบข้อความแสดงวันที่ในหัวตาราง
            const dateOptions = { year: 'numeric', month: 'long', day: 'numeric' };
            document.getElementById('current-date-display').innerText = "ประจำวันที่: " + dateObj.toLocaleDateString('th-TH', dateOptions);

            // เปิดแสดงผลกล่องวิชาเรียน
            document.getElementById('subjectsSection').classList.remove('hidden');

            // ซ่อนปุ่มรายวิชาของทุกวันไว้ก่อน
            document.getElementById('monday-subjects').style.display = 'none';
            document.getElementById('tuesday-subjects').style.display = 'none';
            document.getElementById('wednesday-subjects').style.display = 'none';
            document.getElementById('thursday-subjects').style.display = 'none';
            document.getElementById('friday-subjects').style.display = 'none';
            document.getElementById('weekend-message').style.display = 'none';

            // ตรวจสอบวันแล้วเปิดปุ่มวิชาเฉพาะวันนั้นๆ
            if (dayOfWeek === 1) {
                document.getElementById('day-label').innerText = "📚 รายวิชาเรียนประจำวันจันทร์";
                document.getElementById('monday-subjects').style.display = 'block';
            } else if (dayOfWeek === 2) {
                document.getElementById('day-label').innerText = "📚 รายวิชาเรียนประจำวันอังคาร";
                document.getElementById('tuesday-subjects').style.display = 'block';
            } else if (dayOfWeek === 3) {
                document.getElementById('day-label').innerText = "📚 รายวิชาเรียนประจำวันพุธ";
                document.getElementById('wednesday-subjects').style.display = 'block';
            } else if (dayOfWeek === 4) {
                document.getElementById('day-label').innerText = "📚 รายวิชาเรียนประจำวันพฤหัสบดี";
                document.getElementById('thursday-subjects').style.display = 'block';
            } else if (dayOfWeek === 5) {
                document.getElementById('day-label').innerText = "📚 รายวิชาเรียนประจำวันศุกร์";
                document.getElementById('friday-subjects').style.display = 'block';
            } else {
                // กรณีเลือกวันเสาร์-อาทิตย์
                document.getElementById('day-label').innerText = "📅 ตารางกิจกรรม";
                document.getElementById('weekend-message').style.display = 'block';
            }
        }

        // ฟังก์ชันเมื่อกดเลือกคาบเรียน เพื่อให้ตารางเช็กชื่อและตรวจสอบพฤติกรรมแสดงผลออกมา
        function showAttendance(subjectDetails) {
            document.getElementById('attendance-box').style.display = 'block';
            document.getElementById('current-subject').innerText = 'กำลังตรวจสอบพฤติกรรม: ' + subjectDetails;
        }
    </script>

</body>
</html>
