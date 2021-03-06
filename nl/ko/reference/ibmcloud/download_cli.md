---



copyright:

  years: 2015, 2018
lastupdated: "2018-08-28"

---

{:codeblock: .codeblock}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}


# 독립형 {{site.data.keyword.Bluemix_notm}} CLI 설치
{: #install_use}

{{site.data.keyword.Bluemix_notm}} CLI에서는 {{site.data.keyword.Bluemix_notm}}에서 리소스를 관리하는 명령행 인터페이스를 제공합니다. 여전히 cf CLI를 사용하여 {{site.data.keyword.Bluemix_notm}}에 로그인할 수 있지만 {{site.data.keyword.Bluemix_notm}}에서 Cloud Foundry 서비스와만 작동합니다. 

{{site.data.keyword.Bluemix}} CLI와 {{site.data.keyword.Bluemix_notm}}용 애플리케이션을 개발하기 위해 권장되는 플러그인 및 도구를 모두 설치하려면 [여기](/docs/cli/index.html)에 설명된 방법을 따르십시오.
{: tip}

독립형 {{site.data.keyword.Bluemix_notm}} CLI를 설치하려면 다음 단계를 사용하십시오.

1. 다운로드할 OS의 설치 프로그램 선택

   Mac OS X 64비트: [설치 프로그램](https://clis.ng.bluemix.net/download/bluemix-cli/latest/osx){: new_window} / [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/osx/checksum){: new_window} <br>
   Windows 64비트: [설치 프로그램](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win64){: new_window} / [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win64/checksum){: new_window} <br>
   Linux X86 64비트: [설치 프로그램](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux64){: new_window} / [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux64/checksum){: new_window} <br>
   Linux LE 64비트(ppc64le): [설치 프로그램](https://clis.ng.bluemix.net/download/bluemix-cli/latest/ppc64le){: new_window} / [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/ppc64le/checksum){: new_window} <br>

   32비트 이하 버전의 경우 [모든 버전](/docs/cli/reference/ibmcloud/all_versions.html) 페이지로 이동하여 다운로드하십시오.

1. 설치 프로그램 실행
   * macOS 및 Windows의 경우 설치 프로그램을 실행하십시오.
   * Linux의 경우 패키지의 압축을 풀고 `install` 스크립트를 실행하십시오.

1. API 엔드포인트를 대상으로 지정 및 {{site.data.keyword.Bluemix_notm}}에 로그인

   ```
ibmcloud login
   ```
   {: codeblock}
   
이제 {{site.data.keyword.Bluemix_notm}} 리소스를 관리할 준비가 되었습니다. 명령 설명을 보려면 `ibmcloud help`를 입력하십시오.

연합 ID를 사용하는 경우 [여기](https://console.bluemix.net/docs/iam/login_fedid.html#federated_id)의 지시사항을 따라 일회성 패스코드 또는 API 키로 로그인하십시오.  
{: tip}

설치 프로그램 외에, 다른 방법으로 {{site.data.keyword.Bluemix_notm}} CLI를 설치할 수도 있습니다.

* 쉘에서 설치
* 2진 패키지를 다운로드하여 사용자 정의 디렉토리에 설치

## 쉘에서 설치
{: #shell_install}

### MacOS

다음 명령을 복사하여 Mac OS의 터미널에 붙여넣고 이를 실행하십시오.

```
curl -fsSL https://clis.ng.bluemix.net/install/osx | sh
```
{: codeblock}

### Linux

다음 명령을 복사하여 Linux OS의 터미널에 붙여넣고 이를 실행하십시오.

```
curl -fsSL https://clis.ng.bluemix.net/install/linux | sh
```
{: codeblock}

### Windows PowerShell

다음 명령을 복사하여 [Windows PowerShell](https://msdn.microsoft.com/en-us/powershell/scripting/getting-started/getting-started-with-windows-powershell){: new_window} 터미널 콘솔에 붙여넣고 이를 실행하십시오.

```
iex(New-Object Net.WebClient).DownloadString('https://clis.ng.bluemix.net/install/powershell')
```
{: codeblock}

## 사용자 정의 디렉토리에 설치

설치 프로그램 또는 쉘 스크립트를 사용하여 {{site.data.keyword.Bluemix_notm}} CLI를 설치하는 경우, 바이너리는 시스템 디렉토리에 배치됩니다. 다른 디렉토리를 지정하려는 경우에는 다음 단계를 사용하십시오.

### 1단계: 다음 링크를 사용하여 OS에 따라 2진 패키지를 다운로드하십시오.

|플랫폼 |다운로드 | 체크섬 |
|---------|----------|---------|
|macOS | [tgz](https://clis.ng.bluemix.net/download/bluemix-cli/latest/osx/archive) | [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/osx/archive/checksum) |
| linux32 | [tgz](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux32/archive) | [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux32/archive/checksum) |
| linux64 | [tgz](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux64/archive) | [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux64/archive/checksum) |
| ppc64le | [tgz](https://clis.ng.bluemix.net/download/bluemix-cli/latest/ppc64le/archive) | [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/ppc64le/archive/checksum) |
| win32 | [zip](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win32/archive) | [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win32/archive/checksum) |
| win64 | [zip](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win64/archive) | [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win64/archive/checksum) |

### 2단계: 지정한 디렉토리에 패키지의 압축을 푸십시오.

   패키지의 압축을 푼 후의 컨텐츠는 다음과 같습니다.

   Linux 및 MacOS의 경우

   ```
   IBM_Cloud_CLI
   ├── LICENSE
   ├── NOTICE
   ├── autocomplete
   │   ├── bash_autocomplete
   │   └── zsh_autocomplete
   ├── cfcli
   │   └── cf
   ├── ibmcloud
   └── ibmcloud-analytics
   ```
   {: codeblock}

   Windows의 경우

   ```
   IBM_Cloud_CLI
   ├── LICENSE
   ├── NOTICE
   ├── cfcli
   │   └── cf.exe
   ├── ibmcloud-analytics.exe
   └── ibmcloud.exe
   ```
   {: codeblock}
### 3단계: `PATH` 환경 변수에 추가하고 쉘 자동 완성을 사용으로 설정하십시오.

   * `{YOUR_DIRECTORY}/IBM_CLOUD_CLI`를 `PATH` 환경 변수에 추가하십시오.
   * 쉘 자동 완성 지원(MacOS 및 Linux 전용)에 대해서는 [이 안내서](enable_cli_autocompletion.html)를 참조하십시오.
   
## 독립형 {{site.data.keyword.Bluemix_notm}} CLI 설치 제거

다음 섹션에서는 특정 플랫폼에서 독립형 {{site.data.keyword.Bluemix_notm}} CLI를 설치 제거하는 방법에 대한 세부사항을 제공합니다.

### Windows에서 설치 제거

1. `시작` 단추를 클릭한 후에 `제어판`을 선택하십시오.
2. 팝업 창에서 `프로그램 설치 제거`를 클릭하십시오.
3. 팝업 애플리케이션 목록에서 `IBM Cloud 명령행 인터페이스`를 찾으십시오.
4. `IBM Cloud 명령행 인터페이스`를 마우스 오른쪽 단추로 클릭하고 `설치 제거`를 선택하십시오.
5. 설치 제거 프로그램이 시작됩니다. 지시사항에 따라 설치 제거를 완료하십시오.

### Linux/macOS에서 설치 제거

#### 버전 `0.9.0` 이전

1. 터미널을 열고 다음 명령을 실행하십시오.
  * `rm -rf /usr/local/ibmcloud`
  * `rm -f /usr/local/bin/ibmcloud`
  * `rm -f /usr/local/bin/bluemix`
  * `rm -f /usr/local/bin/bx`
  * `rm -f /usr/local/bin/ibmcloud-analytics`
2. 자동 완성 스크립트를 구성한 경우에는 이를 정리하십시오. 세부사항은 [CLI 자동 완성 사용](enable_cli_autocompletion.html)을 참조하십시오.

#### `0.9.0` 이상

1. 터미널을 열고 다음 명령을 실행하십시오.
  * `/usr/local/ibmcloud/uninstall`
2. 자동 완성 스크립트를 구성한 경우에는 이를 정리하십시오. 세부사항은 [CLI 자동 완성 사용](enable_cli_autocompletion.html)을 참조하십시오.


## {{site.data.keyword.Bluemix_notm}} CLI를 자세히 살펴보기 위한 기타 링크

* [플러그인으로 {{site.data.keyword.Bluemix_notm}} CLI 기능 확장](/docs/cli/reference/ibmcloud/extend_cli.html)
* [{{site.data.keyword.Bluemix_notm}} CLI 참조](/docs/cli/reference/ibmcloud/bx_cli.html)

## 문제 보고 및 피드백 제출
{: #issues}

다음 옵션을 사용하여 문제를 보고하거나 새 기능 요청을 제출하십시오.
 * [Github](https://github.com/IBM-Bluemix/bluemix-cli-release/issues){: new_window} ![외부 링크 아이콘](../../../icons/launch-glyph.svg)에 문제 항목을 작성하십시오.
 * [IBM Cloud 기술에 대한 Slack - #developer-tools 채널](https://ibm-cloud-tech.slack.com)에 메시지를 남기십시오. [여기](https://slack-invite-ibm-cloud-tech.mybluemix.net/){: new_window} ![외부 링크 아이콘](../../../icons/launch-glyph.svg)에서 팀 액세스 권한을 요청하십시오.
