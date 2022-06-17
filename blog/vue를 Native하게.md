# Compile to Native
> Pros
> - 네이티브 코드로 빌드할 수 있다.
> - 네이티브 API에 직접 액세스할 수 있다.
> - 네이티브 앱의 UI를 따를 수 있다.

>Cons
> - HTML을 사용할 수 없고, 프레임워크에서 제공하는 xml 파일로 작성해야 한다.
> - CSS또한 사용할 수 없다.
> - 각 플랫폼별로 다른 컴포넌트를 사용해야 한다.

***
# Framework for Native

Vue를 네이티브 앱으로 변신시켜주는 프레임워크가 몇가지 있다.
프레임워크에 따라 세 가지 범주의 성격을 지닌 앱으로 변환해주는데 `Native App`, `Hybrid App`, `PWA` 성격을 띠는 앱으로 변환이 가능하다.

> - Native App : NativeScript-Vue
> - Hybrid App : Quasar, Ionic vue
> - PWA : Quasar, Nuxt PWA

## NativeScript-Vue
현재 Vue 생태계에서 가장 보편적으로 Native하게 앱을 만드는 솔루션이다.
언제나 그렇듯 장점보다는 지원이 되지 않는 기능들에 초점을 두고 생각해야한다.