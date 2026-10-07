<p align="center"><img src="avatar.png" alt="SCKIMDEV" width="160"></p>

# SCKIMDEV

개인 프로젝트 모음입니다. 저장소는 프로젝트마다 따로 둡니다.

| 저장소 | 서비스 | 주소 | 어떻게 띄우나 |
|---|---|---|---|
| [parking](https://github.com/SCKIMDEV/parking) | 어디에 PARK? — Spring Boot 서버(API) | https://parking.tail7d1054.ts.net | PC 의 Docker 컨테이너(8080)를 Tailscale Funnel 로 공개 |
| [parking-web](https://github.com/SCKIMDEV/parking-web) | 어디에 PARK? — 화면 (서버 API 호출) | https://sckimdev.github.io/parking-web/ | GitHub Pages (정적 페이지) |
| [travel](https://github.com/SCKIMDEV/travel) | Travel Diary — 여행 일정·사진 다이어리 | https://sckimdev.github.io/travel/ | GitHub Pages (정적 페이지) |

```powershell
tailscale funnel --bg --https=443 http://127.0.0.1:8080   # parking
tailscale serve status
```
