# ViewModel

# LiveData

## LiveData와 MutableLiveData의 차이점

LiveData도 변경되는 데이터인데 왜 구분을 지을까?


> ### LiveData
> * LifeCycle의 생명주기를 따른다.
> * 상태가 Destroyed로 변경되면 LiveData도 자동으로 소멸된다. (memory leak X)
> * ViewModel에서 사용되기 때문에 액티비티, 프래그먼트 등의 뷰 컴포넌트가 재실행되어도 ViewModel이 소멸되지 않으므로 LiveData도 소멸되지 않는다.
> * LifeCycle이 활성화 되어있을때 데이터의 변화를 알려주므로 형식적인 코드 사용이 줄어든다.

> ### MutableLiveData
> * LiveData를 상속받고 LiveData의 `setValue()`와 `postValue()`를 구현한 클래스이다.
> * setValue() : 메인스레드에서 즉시 값을 변경하고 옵저버로 데이터 변경을 알려준다.
> * postValue() : Runnable로 데이터 변경 요청, Runnable이 실행될때 데이터 변경, 서브스레드에서 값을 설정하고 메인스레드에서 runnable이 실행되기 전에 `postValue()`가 여러변 호출돼도 마지막 변경된 값만 전달한다.


