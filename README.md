# 1. GO의 특징

## 1.1 병행 프로그래밍에 특화
- Go의 가장 큰 장점은 **간단하면서 강력한 병행성(Concurrency) 지원**이다.
- `goroutine`과 `channel`을 통해 스레드보다 훨씬 가볍고 직관적으로 병행 프로그래밍을 구현할 수 있다.
- 예를 들어, 네트워크 서버나 대규모 데이터 처리 시스템에서 고효율을 발휘한다.  
  _(추후 goroutine, channel에 대한 자세한 설명 필요)_

## 1.2 동적 언어의 개발 속도 + 정적 언어의 안정성
- Go는 **컴파일 기반 정적 타입 언어**이다. → 컴파일 시점에 타입 안정성을 보장.
- 그러나 **인터페이스(Interface)** 를 활용하면 동적 언어처럼 유연한 코드를 작성할 수 있다.
- 이로 인해, **빠른 개발 속도**와 **안정성**을 동시에 확보할 수 있다.

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

# 3. Go Package 설치

원래는 go get ~~~ 이였는데, 
이제는 `go install ~~~@Version` 이런식의 형태이다. 
## 1. Go Doc 설치
ex)
```zsh
    go install golang.org/x/tools/cmd/godoc@latest
```
이제
## 2. Go Docs 로컬에서 확인하기
하단의 명령어를 통해, 확인이 가능
```zsh
    godoc -http=:8080
```