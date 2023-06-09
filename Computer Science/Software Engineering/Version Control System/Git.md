# Git

Git은 소프트웨어 개발에서 코드 버전 관리를 위해 널리 사용되는 무료 및 오픈 소스 분산 버전 관리 시스템입니다. Git은 소프트웨어 프로젝트에서 소스 코드의 이력을 관리하며, 여러 사람들이 동시에 같은 코드를 작업하더라도 서로 충돌하지 않게 해줍니다.

Git의 주요 특징들은 다음과 같습니다:

1. **분산형 시스템:** Git은 분산형 버전 관리 시스템입니다. 이는 각 개발자의 로컬 시스템에 전체 코드베이스의 사본이 저장된다는 뜻입니다. 이는 네트워크 접근 없이도 작업을 계속할 수 있으며, 복구와 백업을 쉽게 만드는 등 다양한 이점을 제공합니다.
2. **브랜치 및 병합:** Git은 브랜치 생성 및 병합을 매우 쉽고 빠르게 만듭니다. 이는 개발자가 서로 다른 기능 또는 버그 수정을 독립적으로 작업하고, 이를 나중에 합칠 수 있게 합니다.
3. **빠른 성능:** Git은 대부분의 명령을 로컬 저장소에서 실행하므로 빠른 성능을 제공합니다.
4. **데이터 무결성:** Git은 내부적으로 체크섬 메커니즘을 사용하여 데이터의 무결성을 보장합니다.
5. **스테이징 영역:** Git에는 '스테이징 영역'이라는 중간 단계가 있습니다. 이는 개발자가 특정 파일들만 선택하여 커밋할 수 있게 해줍니다.
6. **데이터의 전체 히스토리:** Git은 프로젝트의 전체 히스토리를 저장하므로, 언제든지 이전 버전으로 돌아갈 수 있습니다.

Git은 여러 가지 명령어를 통해 제어됩니다. 예를 들어, 'git clone'은 원격 저장소를 복제하는 데 사용되며, 'git commit'은 로컬 변경 사항을 저장소에 기록하는 데 사용됩니다. 'git push'는 로컬 커밋을 원격 저장소에 업로드하는 데 사용되며, 'git pull'은 원격 저장소의 최신 변경 사항을 가져와서 병합하는 데 사용됩니다.

Git을 사용하면서 자주 사용되는 기본적인 명령어들은 다음과 같습니다:

1. **git init:** 새로운 Git 저장소를 초기화합니다. 이 명령어를 실행하면 현재 디렉토리에 **`.git`** 이라는 하위 디렉토리가 생성되고, 이곳에 Git 저장소의 모든 정보와 히스토리가 저장됩니다.
2. **git clone [url]:** 원격 저장소를 로컬에 복제합니다. 이를 통해 원격 저장소의 모든 파일, 히스토리, 브랜치 등을 로컬에 가져올 수 있습니다.
3. **git add [file or .]:** 하나 이상의 파일을 스테이징 영역에 추가합니다. 여기서 '.'는 현재 디렉토리의 모든 변경된 파일을 의미합니다.
4. **git commit -m "commit message":** 스테이징 영역에 있는 변경사항들을 로컬 저장소에 저장합니다. "-m" 옵션 다음에 따옴표 안에 커밋 메시지를 적어줍니다.
5. **git status:** 현재 저장소의 상태를 보여줍니다. 변경된 파일, 스테이징된 파일, 현재 브랜치 등의 정보를 확인할 수 있습니다.
6. **git push [remote] [branch]:** 로컬 저장소의 변경사항들을 원격 저장소에 업로드합니다. **`[remote]`** 에는 원격 저장소의 이름을, **`[branch]`** 에는 업로드할 브랜치의 이름을 적습니다.
7. **git pull [remote] [branch]:** 원격 저장소의 최신 변경사항들을 로컬 저장소에 가져와서 병합합니다.
8. **git branch [branch-name]:** 새로운 브랜치를 생성합니다.
9. **git checkout [branch-name]:** 지정한 브랜치로 전환합니다.
10. **git merge [branch]:** 다른 브랜치의 변경사항들을 현재 브랜치에 병합합니다.
11. **git log:** Git 저장소의 커밋 히스토리를 시간 순서대로 보여주는 명령어입니다.
12. **git reset [commit id]:** 특정 파일, 커밋 또는 브랜치를 이전 상태로 되돌리는 Git 명령어입니다.
- --hard : 변경된 내용을 완전히 삭제하고 이전 상태로 되돌림
- --mixed : 변경 이력은 모두 삭제하지만 변경 내용은 남아있음
- --soft : 변경 이력은 모두 삭제하지만 변경 내용은 남음. 그러나 stage 되어있음.
13. **git revert [commit id]:** 이전 커밋의 변경 사항을 취소하고, 이전 상태로 되돌리는 대신 새로운 커밋을 생성하여 이전 상태로 돌아가는 Git 명령어입니다.

위의 명령어들은 Git을 사용하면서 가장 기본적으로 알아야 하는 명령어들입니다. Git은 매우 강력한 도구로서, 이 외에도 수많은 고급 명령어와 옵션들을 지원합니다.