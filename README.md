# 1. GO의 특징

## 1. 병행 프로그래밍의 특화
- GoRoutine > 추후 자세한 설명 필요!

## 2. 동적언어의 개발 속도와 정적언어의 안정성을 가진다.
-   컴파일 기반의 정적 타입언어 이지만, Go의 인터페이스를 통해, 동적 언어의 장점을 일부 수용한다. 

# 2. GO 언어의 설치

## 1. Mac
### 1. Brew Package Manager로 설치
```zsh
    brew install go
```

### 2. GO 개발을 위한 작업공간 설정

```zsh
mkdir -p $HOME/go
```

### 3. 환경 변수 입력
``` zsh
# ~/.zshrc

# Path to Go in HomeBrew
export PATH=$PATH:/usr/local/opt/go/libexec/bin
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
```

### 4.프로젝트 디렉토리 생성하기
```zsh
    go mod init $myProject
```