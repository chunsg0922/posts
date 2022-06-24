# Application Class
안드로이드의 Application Class는 애플리케이션 컴포넌트 사이에서 공통으로 멤버들을 사용할 수 있게 해주는 편리한 공유 클래스를 제공한다.

즉, 애플리케이션 사이의 컴포넌트들이 공통으로 사용할 내용을 작성하면 context를 이용하여 어느 컴포넌트에서든 접근이 가능해지도록 만들어준다.

## 사용방법
1. Application Class를 상속받는 Class를 만든다.
2. AndroidManifest.xml에 Application Class name을 추가한다.
3. 애플리케이션 내의 컴포넌트들 사이에서 context를 이용한 접근이 가능하다.(데이터 공유)

> 다음은 Application Class를 상속받는 Application 기능 클래스를 정의한 것이다.
```Kotlin
public calss MyApplication : Application(){

    companion object{
        lateinit var instance : MyApplication
        private set

        fun context() : Context {
            return instance.applicationContext
        }
    }

    override fun onCreate(){
        super.onCreate()
        instance = this
    }
}

```

> 다음으로 AndroidManifest.xml에 Application 설정을 한다.
``` xml


``` 