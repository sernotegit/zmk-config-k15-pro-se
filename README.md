# Keychron K15 Pro SE ZMK Custom Configuration

키크론 **K15 PRO SE ZMK (Alice 75% 슬림 무선)** 키보드를 위한 커스텀 ZMK 설정 저장소입니다.  
Realtek RTL8762G 무선 SoC 칩셋에 최적화된 ZMK 펌웨어를 GitHub Actions를 통해 자동으로 빌드합니다.

---

## 🚀 적용된 커스텀 기능

### 1. 캡스락 키 (Tap-Hold)
* **Tap**: `Space` (일반 스페이스 입력)
* **Hold**: `Layer 1` (Mac 모드) / `Layer 3` (Windows 모드) Fn 레이어 활성화
* **고급 파라미터 적용**:
  * `flavor = "balanced"`: 다른 키와 조합 시 레이어로 즉시 판정
  * `quick-tap-ms = <175>`: 연타 시 레이어가 켜지지 않고 스페이스 연속 입력
  * `retro-tap`: 길게 누르고 있다가 다른 키 입력 없이 떼면 스페이스 정상 출력

### 2. 콤보 (Combos) 매핑
동시에 누를 때 발동되는 콤보입니다 (`timeout-ms = <40>`):

| 콤보 키 | 동작 | 세부 기능 |
|:---:|:---:|:---|
| **`W` + `E`** | `&kp CAPS` | 캡스락 켜기/끄기 |
| **`S` + `D`** | `&kp RALT` | 한/영 전환 (우측 Alt) |
| **`D` + `F`** | `&kp SPACE` | 스페이스 입력 |
| **`J` + `K`** | `&kp ENTER` | 엔터 입력 |
| **`Z` + `X`** | `&kp LC(X)` | 잘라내기 (Ctrl+X) |
| **`X` + `C`** | `&kp LC(C)` | 복사하기 (Ctrl+C) |
| **`C` + `V`** | `&kp LC(V)` | 붙여넣기 (Ctrl+V) |

---

## 🛠️ 펌웨어 빌드 및 플래싱 방법

### 1. 자동 빌드 펌웨어 다운로드
1. GitHub 저장소 상단의 **Actions** 탭으로 이동합니다.
2. 최신 워크플로우 실행 항목을 클릭합니다.
3. 하단 **Artifacts** 섹션에서 `k15_pro_se_firmware.zip`을 다운로드하고 압축을 풉니다.
4. 압축 해제 시 `k15_pro_se_zmk.bin` 파일이 생성됩니다.

### 2. 키보드 플래싱 (Keychron Launcher)
1. 키보드 후면 스위치를 **Cable(유선)** 모드로 전환하고 USB-C 케이블로 PC와 연결합니다.
2. 크롬 또는 엣지 브라우저에서 [Keychron Launcher](https://launcher.keychron.com/)에 접속합니다.
3. 좌측 메뉴의 **[Firmware Upgrade]** 탭으로 이동합니다.
4. 키보드를 연결하고, 다운로드받은 `k15_pro_se_zmk.bin` 파일을 업로드하여 플래싱을 진행합니다.
