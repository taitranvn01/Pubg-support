# PUBG-Support

## Giới thiệu / Overview

Tiếng Việt:
Thư mục `Pubg-support` chứa tài nguyên hỗ trợ liên quan đến PUBG (scripts, cấu hình, media, hướng dẫn). File này cung cấp hướng dẫn cài đặt và sử dụng cơ bản trên Windows.

English:
The `Pubg-support` folder contains support resources for PUBG (scripts, configs, media, guides). This README provides basic installation and usage instructions for Windows.

---

## Mục lục / Table of contents

- [Yêu cầu / Requirements](#y%C3%AAu-c%E1%BA%A7u--requirements)
- [Cài đặt nhanh (Windows) / Quick install (Windows)](#c%C3%A0i-%C4%91%E1%BA%B7t-nhanh-windows--quick-install-windows)
- [Cấu hình / Configuration](#c%E1%BA%A5u-h%C3%ACnh--configuration)
- [Sử dụng / Usage](#s%E1%BB%AD-d%E1%BB%A5ng--usage)
- [Khắc phục sự cố / Troubleshooting](#kh%E1%BA%A9c-ph%E1%BB%A5c-s%E1%BB%B1-c%E1%BB%A7u--troubleshooting)
- [Góp ý / Contributing](#g%C3%B3p-%C3%BD--contributing)
- [Giấy phép / License](#gi%E1%BA%A5y-ph%C3%A9p--license)

---

## Yêu cầu / Requirements

Tiếng Việt:
- Windows 10/11 (64-bit) đã cập nhật.
- Quyền Administrator cho một số thao tác (ví dụ: thay PATH, cài phần mềm).
- Có thể cần: `ffmpeg`, `Node.js`, hoặc `Python` — tùy theo script trong thư mục.

English:
- Windows 10/11 (64-bit).
- Administrator rights for some setup steps.
- Possible dependencies: `ffmpeg`, `Node.js`, `Python` depending on included scripts.

---

## Cài đặt nhanh (Windows) / Quick install (Windows)

Lưu ý: các bước dưới đây là hướng dẫn tổng quát; điều chỉnh theo nội dung thực tế trong `Pubg-support`.

Tiếng Việt — Các bước cơ bản:
1. Mở PowerShell với quyền Administrator.
2. Điều hướng tới thư mục `Pubg-support`:

```powershell
cd "D:\Pubg-support"
```

3. Nếu cần `ffmpeg`: nếu đã có bản nén trong thư mục (ví dụ `ffg\`), thêm đường dẫn `bin` vào PATH tạm thời hoặc vĩnh viễn.

Tạm thời (phiên hiện tại):

```powershell
$env:Path += ";D:\ffg\ffmpeg-master-latest-win64-gpl\bin"
```

Thêm vĩnh viễn (Administrator):

```powershell
setx /M PATH "%PATH%;D:\ffg\ffmpeg-master-latest-win64-gpl\bin"
```

4. Cài Node.js hoặc Python nếu script yêu cầu (tải từ trang chính thức và chạy installer).
5. Nếu thư mục có script cài đặt (ví dụ `install.ps1`, `setup.bat`), chạy theo hướng dẫn:

```powershell
# PowerShell script
.\install.ps1

# batch file
.\setup.bat
```

6. Cài dependencies nếu cần:

```powershell
# Node.js project
npm install

# Python project
pip install -r requirements.txt
```

English — Basic steps:
1. Open PowerShell as Administrator.
2. cd into `D:\Pubg-support`.
3. Make `ffmpeg` available if required (add local `ffg\...\bin` to PATH temporarily or permanently).
4. Install Node.js or Python if scripts require them.
5. Run any included install/setup scripts (e.g. `install.ps1`, `setup.bat`).
6. Install dependencies with `npm install` or `pip install -r requirements.txt` as needed.

---

## Cấu hình / Configuration

Tiếng Việt:
- Kiểm tra các file cấu hình (.json, .yml, .conf) và chỉnh đường dẫn, token, hoặc tùy chọn.
- Thiết lập biến môi trường bằng `setx` (vĩnh viễn) hoặc `$env:NAME = "value"` (tạm thời).

English:
- Inspect config files and update paths, tokens, or user settings.
- Use `setx` for persistent env vars or `$env:NAME = "value"` for the current session.

---

## Sử dụng / Usage

### Scene APK Installation (Hướng dẫn cài đặt Scene trên Android)

Tiếng Việt:
Thư mục `scene/` chứa các file APK của ứng dụng Scene cho thiết bị Android phiên bản khác nhau:
- `scene_8.3.0 Alpha2.apk`
- `scene_9.1.0.apk`
- `scene_9.1.1.apk`
- `scene_9.2.0 Alpha9.apk`
- `scene_9.2.0 Beta1.apk`

**Hướng dẫn cài đặt trên Android:**
1. Sao chép file APK từ `D:\Pubg-support\scene\` vào điện thoại Android (qua USB, email, cloud, hoặc tải xuống trực tiếp).
2. Trên điện thoại Android, vào **Settings** (Cài đặt) → **Security** (Bảo mật) hoặc **Privacy** (Quyền riêng tư) → bật **Unknown Sources** (cho phép cài đặt từ nguồn không xác định).
3. Mở **File Manager** (Trình quản lý tệp), tìm file APK vừa sao chép.
4. Nhấn vào file APK và chọn **Install** (Cài đặt).
5. Chờ quá trình cài đặt hoàn tất.
6. Nhấn **Open** (Mở) để khởi chạy ứng dụng Scene.

English:
The `scene/` folder contains multiple versions of the Scene APK application for Android devices:
- `scene_8.3.0 Alpha2.apk`
- `scene_9.1.0.apk`
- `scene_9.1.1.apk`
- `scene_9.2.0 Alpha9.apk`
- `scene_9.2.0 Beta1.apk`

**Installation steps on Android:**
1. Transfer the APK file from `D:\Pubg-support\scene\` to your Android device (via USB, email, cloud storage, or direct download).
2. On your Android phone, go to **Settings** → **Security** (or **Privacy**) → enable **Unknown Sources** (allow installation from unknown sources).
3. Open **File Manager** and locate the APK file.
4. Tap the APK file and select **Install**.
5. Wait for the installation to complete.
6. Tap **Open** to launch the Scene app.

---

### PC Usage / Sử dụng trên PC

Tiếng Việt:
- Các lệnh chạy thường gặp (tùy theo nội dung):

```powershell
# PowerShell script
.\run-support.ps1

# Node.js
node index.js

# Python
python script.py
```

English:
- Run scripts or programs on this PC. Examples above show common commands for PowerShell, Node, and Python.

---

## Khắc phục sự cố / Troubleshooting

Tiếng Việt:
- "is not recognized" → kiểm tra PATH và vị trí file thực thi.
- Lỗi phụ thuộc → chạy `npm install` hoặc `pip install -r requirements.txt`.
- Lỗi chính sách thực thi PowerShell:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
```

English:
- "is not recognized" → check PATH and executable presence.
- Dependency errors → run `npm install` or `pip install -r requirements.txt`.
- PowerShell execution policy issues:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
```

---

## Góp ý / Contributing

Tiếng Việt:
- Thêm mô tả cho scripts/configs mới và mở issue/PR nếu dùng git.

English:
- Add descriptive files for new scripts/configs and open an issue/PR when using version control.

## Support by Tai 

Please follow me =))

 README: created on 2026-03-04_