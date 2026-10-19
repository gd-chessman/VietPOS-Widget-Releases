# VietPOS-Widget-Releases

Repo **public** phát hành APK [VietPOS Widget](https://github.com/gd-chessman/VietPOS-Widget-Releases).

## Cách phát hành bản mới

1. Build APK release (cùng keystore mọi bản).
2. Tạo **GitHub Release** (tag ví dụ `v0.2.4`), upload `VietPOS-Widget-release.apk`.
3. Cập nhật **`latest.json`** trên nhánh `main`:
   - `versionCode` — phải **lớn hơn** bản đang cài trên máy (integer trong `build.gradle.kts`).
   - `apkUrl` — link tải trực tiếp, dạng  
     `https://github.com/gd-chessman/VietPOS-Widget-Releases/releases/download/<tag>/VietPOS-Widget-release.apk`
   - `versionName`, `releaseNotes` — tuỳ chọn.

App widget đọc trực tiếp:

`https://raw.githubusercontent.com/gd-chessman/VietPOS-Widget-Releases/main/latest.json`

(nếu thiếu hoặc lỗi, thử GitHub API **Releases latest** + file `.apk`) → popup cập nhật, tải APK từ `apkUrl`.
