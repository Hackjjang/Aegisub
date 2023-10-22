## arch1t3cht's Aegisub "fork"
릴리스 빌드는 [여기](https://github.com/arch1t3cht/Aegisub/releases) 또는 최신 CI 빌드는 [여기](https://github.com/arch1t3cht/Aegisub/actions)에서 다운로드하세요.

릴리스 페이지에는 모든 변경 사항과 새로운 기능에 대한 자세한 목록도 있습니다. 기술적인 세부 사항에 관심이 있거나 직접 컴파일하고 싶다면 계속 읽어보세요.

### 이미 Aegisub 포크가 충분하지 않나요?
물론 그렇고, 또 다른 포크를 추가하는 것이 [서류상으로는](https://xkcd.com/927/) [좋은 생각이 아닌 것 같다는 건](https://cdn.discordapp.com/attachments/425357202963038208/1007103606421459004/unknown.png) 알고 있습니다. 하지만,

- 현재 존재하는 포크 중 어느 것도 완전히 만족스럽지 않습니다:
  - [wangqr's fork](https://github.com/wangqr/Aegisub)가 활발히 유지되고 있지만 안정성에 더 초점을 맞추고 있습니다. 대부분의 최신 기능이 누락되어 있습니다.
  - [AegisubDC](https://github.com/Ristellise/AegisubDC)는 가장 최신 기능(특히 비디오 패닝)을 제공하지만 윈도 전용이며 더 이상 활발하게 유지 관리되지 않습니다.
  - [The TypesettingTools fork](https://github.com/TypesettingTools/Aegisub)는 언젠가 업스트림 버전이 될 것이며 모든 운영 체제에서 비교적 쉽게 빌드할 수 있지만 현재로서는 크게 움직이지 않고 있습니다. 이 포크의 기반이며, 언젠가는 이 추가 기능의 대부분을 이 포크에 병합할 수 있기를 바랍니다.
- 여기서의 변경 사항을 여러 포크에 홍보하는 것만으로는 더 큰 혼란을 야기할 수 있습니다.
- 저는 이번 포크가 확장된 지원과 안정성 수정을 목표로 하는 전통적인 의미의 "포크"가 아니라고 스스로를 설득하려고 노력합니다. 다른 포크에서 떠돌아다니는 가장 중요한 새로운 기능들과 함께 제가 직접 만든 새로운 기능들의 모음입니다 ~~ 이 시점에서 여전히 이런 말을 하기에는 너무 늦었을 것입니다. 그래도 일반적인 미션은 변하지 않았습니다. 이 포크는 새로운 기능과 중요한 버그 수정을 수집하지만 정리 및 리팩터와 같은 유지 관리 측면에는 추가 시간을 투입하지 않을 것입니다. 이는 대규모 리팩터링으로 인해 이러한 변경 사항을 업스트림 리포지토리나 향후 포크로 가져오기가 더 어려워지기 때문이기도 합니다.

    현재 제가 사용하고 있는 Aegisub 버전도 이 버전이지만, 안정성에 대해서는 장담할 수 없습니다. 이 버전은 주로 조판 및 기타 고급 용도로만 사용해야 하므로 아무 버전이나 찾고 있다면 **사용하지 마세요.**

### 조직
이 저장소는 다양한 기능 추가의 모음이기 때문에 다른 저장소에 쉽게 병합할 수 있도록 다양한 기능에 대한 브랜치 집합으로 구성됩니다. [`기능`](https://github.com/arch1t3cht/Aegisub/tree/feature) 브랜치는 현재 사용 가능하다고 판단되는 모든 기능을 병합합니다. 리포지토리의 구조상 이 브랜치와 일부 개별 브랜치를 매우 자주 강제 푸시할 것이므로 추가 브랜치의 기반이 되기에 이상적이지 않습니다.

`cibuilds` 브랜치는 관련 시점에 `기능`의 스냅샷에 대한 일부 CI 빌드를 만든다.

### 브랜치/기능 목록
이 목록은 저장소를 탐색하기 위한 것입니다. 보다 체계적인 변경 로그는 [릴리스 페이지](https://github.com/arch1t3cht/Aegisub/releases)로 이동하세요.
- [`folding`](https://github.com/arch1t3cht/Aegisub/tree/folding) : 자막 그리드에서 선을 시각적으로 그룹화하고 접는 기능을 추가합니다.
- [`lua_api`](https://github.com/arch1t3cht/Aegisub/tree/lua_api) : 텍스트 편집 상자에서 선택 또는 커서 제어와 같은 새로운 기능을 Lua 자동화 API에 추가합니다.
- [`vector_clip_actions`](https://github.com/arch1t3cht/Aegisub/tree/vector_clip_actions) : 벡터 클립 도구의 다양한 모드(선, 베지어 곡선, 포인트 추가 등)를 단축키에 할당할 수 있도록 합니다.
- [`color_picker_fix2`](https://github.com/arch1t3cht/Aegisub/tree/color_picker_fix2) : 색상 선택기를 창으로 제한하는 옵션('인터페이스' 아래)을 추가하여 리눅스에서 색상 선택기가 많은 경우 수정됩니다.
- [`avisynth`](https://github.com/arch1t3cht/Aegisub/tree/avisynth) : 윈도에서 Avisynth 지원을 다시 활성화하고 리눅스에서 Avisynth를 활성화합니다.
- [`bestsource`](https://github.com/arch1t3cht/Aegisub/tree/bestsource) : BestSource 오디오 및 비디오 소스를 추가합니다. 이 소스는 다른 소스보다 몇 배나 느리지만 그 대신 정확한 탐색을 보장할 수 있습니다.
- [`vapoursynth`](https://github.com/arch1t3cht/Aegisub/tree/vapoursynth) : Vapoursynth 오디오 및 비디오 소스 추가
- [`bugfixes`](https://github.com/arch1t3cht/Aegisub/tree/bugfixes) : 컴파일에 필요한 다양한 수정. 대부분의 브랜치는 이것을 기반으로 합니다.
- [`workarounds`](https://github.com/arch1t3cht/Aegisub/tree/workarounds) : `버그 수정` 같지만, 더 많은 작업 없이는 가져와서는 안 되는 해킹성 수정입니다.
- [`fixes`](https://github.com/arch1t3cht/Aegisub/tree/fixes): 기타 버그 수정
- [`misc`](https://github.com/arch1t3cht/Aegisub/tree/misc): 기타 기타 추가
- [`wangqr_gui`](https://github.com/arch1t3cht/Aegisub/tree/wangqr_gui): GUI와 관련된 wangqr의 변경 사항을 병합합니다. 특히, 높은
- - [`wangqr_gui`](https://github.com/arch1t3cht/Aegisub/tree/wangqr_gui): GUI와 관련된 wangqr의 변경 사항을 병합합니다. 특히 높은 DPI 호환성을 추가하세요.
- [`misc_dc`](https://github.com/arch1t3cht/Aegisub/tree/misc_dc): AegisubDC에서 가져온 기타 변경 사항
- [`xa2-ds`](https://github.com/arch1t3cht/Aegisub/tree/xa2-ds): XAudio2 백엔드를 추가하고 wangqr 및 Shinon의 일부 다른 백엔드에 대한 스테레오 재생을 허용합니다.
- [`stereo`](https://github.com/arch1t3cht/Aegisub/tree/stereo): 가능한 경우 다른 오디오 백엔드에 대한 다중 채널 지원을 추가합니다.
- [`video_panning_option`](https://github.com/arch1t3cht/Aegisub/tree/video_panning_option): [moex3의 비디오 확대/축소 및 패닝](https://github.com/TypesettingTools/Aegisub/pull/150) 병합, 몇 가지 버그 수정 및 확대/축소 동작 제어를 위한 추가 옵션 포함
- [`spectrum-frequency-mapping`](https://github.com/arch1t3cht/Aegisub/tree/spectrum-주파수-mapping): EleonoreMizo의 [스펙트럼 디스플레이 개선](https://github.com/TypesettingTools/) 병합 Aegisub/pull/94), Shift+Scroll을 사용하여 오디오 디스플레이를 수직으로 확대/축소할 수도 있습니다.
- [`wangqr_time_video`](https://github.com/arch1t3cht/Aegisub/tree/wangqr_time_video): 동영상 변경 사항에 자막 타이밍 도구를 추가하는 wangqr 기능을 병합합니다.

### 문제 해결
버그 보고서를 기꺼이 받아들이겠지만, 문제가 발생하면 먼저 내 포크에서만 발생하는지, 아니면 [이전 TSTools 빌드](https://github.com/TypesettingTools/Aegisub/actions)에서도 발생하는지 확인하세요. .
내 포크로 소개되지 않았다면 살펴볼 수는 있지만 약속할 수는 없습니다.

아래 링크된 Cave 및 TSTools 서버를 포함한 다양한 서버에서 지원을 받으려면 저를 찾으세요.

#### 리눅스의 Aegisub이 내 GTK 테마를 인식하지 못합니다.
이는 아마도 wxgtk2를 사용하여 빌드하고 있기 때문일 것입니다. wxgtk3을 사용하여 빌드하면 이 문제가 해결되지만 그 자체로 몇 가지 문제가 발생합니다(특히 깨진 색상 선택기, 자동화 스크립트에서 파일 대화 상자를 열 때 가끔 충돌 및 일반 레이아웃 문제).

정확한 전환 방법은 리눅스 배포판에 따라 다르지만 기본적으로 `wx-config` 또는 그 다음으로 가장 좋은 변형이 wxgtk3을 가리키는지 확인해야 합니다. 기본적으로 wxgtk2를 가리키고 wxgtk2 제거가 옵션이 아닌 경우 임시로 경로 밖으로 이동하거나 중간자 프로젝트에서 `native-file`을 사용할 수도 있습니다. 그런 다음 'mesonconfigure --clearcache' 및 'meson setup --reconfigure'를 사용하여 meson을 완전히 재구성하세요.

#### 동영상이 비동기화됨/프레임이 적절한 시간에 표시되지 않음
이는 아마도 ffms2 탐색 버그([#394](https://github.com/FFMS/ffms2/issues/394)) 때문일 수 있습니다. 윈도에서는 이러한 특정 회귀가 더 이상 발생하지 않습니다. 리눅스에서는 ffms2의 최신 git 버전을 설치해야 합니다. 예를 들어 아치 리눅스의 [`ffms2-git`](https://aur.archlinux.org/packages/ffms2-git) AUR 패키지를 설치하거나 그냥 컴파일해야 합니다. 스스로요.

이 특정 버그 때문이 아닌 경우 Avisynth, Vapoursynth 또는 BestSource를 통해 LSMASHSource와 같은 대체 비디오 소스를 사용해 볼 수도 있습니다.

#### 윈도 : 비디오를 열 때마다 Aegisub가 충돌합니다.
직접 컴파일하는 경우 meson 옵션에 `--force-fallback-for=zlib`를 추가해 보세요.


### 편집
Aegisub만 설치하려는 경우 [릴리스 페이지](https://github.com/arch1t3cht/Aegisub/releases) 또는 [CI 빌드](https://github.com)를 확인하는 것이 좋습니다. /arch1t3cht/Aegisub/actions) 먼저.

윈도에서의 컴파일에 대해서는 아래 TSTools 설명서를 참조하세요. 또한 프로젝트 인수에 대해서는 [GitHub 워크플로](https://github.com/arch1t3cht/Aegisub/blob/cibuilds/.github/workflows/ci.yml)를 확인하세요.

아치 리눅스에는 [aegisub-arch1t3cht-git](https://aur.archlinux.org/packages/aegisub-arch1t3cht-git)이라는 AUR 패키지가 있습니다. 내가 관리하지는 않지만 작동하는 것 같습니다.

다른 리눅스 배포판이나 수동 컴파일의 경우 특히 필요한 설치를 위해 이 패키지나 [TSTools PKGBUILD](https://aur.archlinux.org/packages/aegisub-ttools-meson-git)를 참조로 사용할 수 있습니다. 직접 컴파일하고 싶지 않은 경우 종속성.
모든 종속성이 설치된 경우 :
- Meson 설치
- 저장소를 복제합니다.
- 저장소에서 기본 구성을 위해 `meson setup build --buildtype=release`를 실행합니다. 추가 옵션은 아래를 참조하세요.
- `build` 디렉토리에 `cd`를 추가하고 `ninja`를 실행합니다.
- `build` 폴더에 `aegisub` 바이너리가 생성됩니다. 시스템 전체 위치에 설치하려면 'ninja install'을 실행하세요. `/usr/local` 대신 `/usr`에 설치하려면 meson을 구성하거나 재구성할 때 `--prefix=/usr`을 전달하세요.
- 새 커밋을 가져온 후 다시 컴파일할 때 'meson setup' 설정을 건너뛰고 빌드 디렉터리에서 즉시 'ninja'를 실행하세요. 빌드 구성이 변경된 경우에도 마찬가지입니다.

#### 컴파일 플래그
일부 기능은 기본적으로 활성화되어 있지 않습니다. 이를 활성화하려면 `meson setup` 명령과 함께 `-D<feature>=enabled`를 전달하세요.

- `-Davisynth=enabled` : Avisynth 지원
- `-Dbestsource=enabled` : BestSource
- `-Dvapoursynth=enabled` : Vapoursynth 지원

동일한 방식으로 기본적으로 활성화된 옵션을 비활성화할 수도 있습니다. 모든 옵션은 `meson_options.txt` 파일을 확인하세요.

기존 빌드 디렉터리의 옵션을 변경하려면 `build` 디렉터리 내부에서 `meson setup --reconfigure <new arguments>`를 실행하세요.

### 종속성
TSTools 버전에 대한 종속성 외에도 몇 가지 추가 종속성이 있습니다. 찾을 수 없는 경우 처음부터 복제 및 컴파일되지만 대신 바이너리를 설치할 수도 있습니다.
- `jansson` : BestSource용
- `ffmpeg` : BestSource로 컴파일할 때 직접적인 종속성이 됩니다.
- `avisynth`(또는 `avisynthplus`) : Avisynth 소스에 대한 선택적 런타임 종속성
- `vapoursynth` : VapourSynth 소스에 대한 선택적 런타임 종속성

    다음 VapourSynth 플러그인은 기본 구성에 설정된 기본 스크립트에 의해 사용됩니다:
    - [`lsmas`](https://github.com/AkarinVS/L-SMASH-Works) : LWLibavSource용
    - [`bas`](https://github.com/vapoursynth/bestaudiosource) : BestAudioSource용
    - [`wwxd`](https://github.com/dubhater/vapoursynth-wwxd) 및 [`scxvid`](https://github.com/dubhater/vapoursynth-scxvid)(설정에 따라 다름) : 키프레임용 세대


# Aegisub

바이너리 및 일반정보는 [홈페이지 참조](http://www.aegisub.org)를 참조하세요.

버그 추적기는 https://github.com/Aegisub/Aegisub/issues에서 찾을 수 있습니다.

지원은 [Discord](https://discord.com/invite/AZaVyPr) 또는 [IRC](irc://irc.rizon.net/aegisub)에서 가능합니다.

## Aegisub 빌드

### 윈도

전제 조건 :

1. Visual Studio(최신 버전의 커뮤니티 에디션이면 충분)
2. 2010년 6월 DirectX SDK(DirectSound가 삭제되기 전 최종 릴리스)
3. 파이썬 3
4. Meson
5. CMake
6. Powershell 실행 정책이 무제한으로 설정됨

경에 설치해야 하는 몇 가지 선택적 종속성이 있습니다.

1. msgfmt, 번역 작성
2. InnoSetup, 일반 설치 프로그램 빌드
3. 7zip, 일반 설치 프로그램 빌드
4. 일반 설치 프로그램을 빌드하기 위한 Moonscript

다른 모든 종속성은 저장소에 저장되거나 하위 모듈로 포함됩니다.

빌드 :

1. Aegisub 저장소 복제: `git clone https://github.com/arch1t3cht/Aegisub.git`
2. Visual Studio "x64 기본 도구 명령 프롬프트"에서 빌드 디렉터리 `meson build -Ddefault_library=static`(릴리스용으로 빌드하는 경우 `--buildtype=release` 추가)을 생성합니다.
3. `cd build`와 `ninja`를 사용하여 빌드

이제 `aegisub.exe`라는 바이너리가 있어야 합니다.

설치 프로그램 :

성공적인 빌드 후에 `ninja win-installer`를 사용하여 설치 프로그램을 생성할 수 있습니다. 이는 인터넷 연결이 작동하고 선택적 종속성이 설치되어 있다고 가정합니다.

성공적인 빌드 후에 `ninja win-portable`을 사용하여 휴대용 zip을 생성할 수 있습니다.

### OS X

막연하게 최신 버전의 Xcode와 해당 명령줄 도구가 필요합니다.

개인적인 용도의 경우 pip 및 홈브류를 사용하여 거의 모든 Aegisub의 종속성을 설치할 수 있습니다.

    pip3 install meson
    brew install cmake ninja pkg-config  libass boost zlib ffms2 fftw hunspell
    export LDFLAGS="-L/usr/local/opt/icu4c/lib"
    export CPPFLAGS="-I/usr/local/opt/icu4c/include"
    export PKG_CONFIG_PATH="/usr/local/opt/icu4c/lib/pkgconfig"

종속성이 설치되면 'meson build && meson compile -C build'를 사용하여 Aegisub를 빌드합니다.

#### dmg 빌드

```bash
meson build_static -Ddefault_library=static -Dbuildtype=debugoptimized -Dbuild_osx_bundle=true -Dlocal_boost=true
meson compile -C build_static
meson test -C build_static --verbose
meson compile osx-bundle -C build_static
meson compile osx-build-dmg -C build_static
```

## Moonscript 업데이트

Moonscript 저장소 내에서 `bin/moon bin/splat.moon -l moonscript moonscript/ > bin/moonscript.lua`를 실행하세요.
새로 생성된 `bin/moonscript.lua`를 열고 그 안에서 다음과 같이 변경합니다.

1. 파일의 마지막 줄 `package.preload["moonscript"]()` 앞에 `return`을 추가하여 `return package.preload["moonscript"]()`를 생성합니다.
2. `package.preload['moonscript.base']`의 함수 내에서 `moon_loader`, `insert_loader` 및 `remove_loader`에 대한 참조를 제거합니다. 이는 반환된 테이블에서 선언, 정의 및 항목을 제거하는 것을 의미합니다.
3. `package.preload['moonscript']`의 함수 내에서 `_with_0.insert_loader()` 줄을 제거합니다.

이제 파일을 사용할 준비가 되었으며 Aegisub 저장소 내의 `automation/include`에 배치됩니다.

## 라이선스

이 저장소의 모든 파일은 다양한 GPL 호환 BSD 스타일 라이선스에 따라 라이선스가 부여됩니다. 자세한 내용은 라이선스 및 개별 소스 파일을 참조하세요.
공식 윈도 및 OS X 빌드는 fftw3을 포함하므로 GPLv2입니다.
