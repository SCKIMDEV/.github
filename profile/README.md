# SCKIMDEV

한 PC(Tailscale 이름 `parking`)에서 운용하는 개인 서비스들입니다. 저장소는 서비스마다 따로 두고, 바깥 주소는 **포트로 구분**합니다.

| 저장소 | 서비스 | 로컬 포트 | 주소 | 공개 범위 |
|---|---|---|---|---|
| [parking](https://github.com/SCKIMDEV/parking) | 어디에 PARK? — Spring Boot 주차장 검색 | 8080 | https://parking.tail7d1054.ts.net | Funnel (인터넷 공개) |
| [travel](https://github.com/SCKIMDEV/travel) | Travel Diary — 여행 일정·사진 다이어리 | 8787 | https://parking.tail7d1054.ts.net:8443 | 테일넷 전용 |

라우팅은 PC의 Tailscale Serve 설정이 맡습니다.

```powershell
tailscale funnel --bg --https=443  http://127.0.0.1:8080   # parking
tailscale serve  --bg --https=8443 http://127.0.0.1:8787   # travel
tailscale serve status
```

각 서비스는 자기 폴더에서 `docker compose up -d` 로 따로 올리고 내립니다.
