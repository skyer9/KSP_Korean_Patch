
소스코드는 아래 사이트에서 가져왔습니다.
from https://github.com/sarbian/KerbalFontProject



한글폰트 생성방법은 아래와 같습니다.

1. unity 5.2.x 버전 설치(반드시 5.4 이전 버전을 설치해아 한다.)

2. unity 를 실행하고 새 프로젝트를 생성한다.

3. Assets 폴더에 아래 폴더를 생성한다.

 - Assets\AssetBundles
 - Assets\Editor
 - Assets\Fonts
 - Assets\Resources
 - Assets\Resources\Fonts & Materials

4. 폰트를 추가한다.

Assets\Fonts 폴더에 NotoSansCJKkr-Light.otf 를 복사해 넣는다.
Assets 폴더에 KS1001.txt 를 복사해 넣는다.

5. 에셋번들 생성 스크립트 추가

Assets\Editor 에 CreateAssetBundles.cs 를 생성한다.
내용은 아래와 같다.

// =============================================================================
using UnityEditor;

public class CreateAssetBundles
{
    [MenuItem("Assets/Build AssetBundles")]
    static void BuildAllAssetBundles()
    {
        BuildPipeline.BuildAssetBundles("Assets/AssetBundles", BuildAssetBundleOptions.None, BuildTarget.WebPlayer);
    }
}
// =============================================================================

4. Text Mesh Pro 설치

5. 폰트 에셋 생성 및 저장

메뉴 > Window > TextMeshPro - Font Asset Creator 실행

Assets\Resources\Fonts & Materials 플더에 생성된 NotoSansCJKkr-Light SDF.asset 를 넣어준다.

6. 에셋 라벨을 지정해 준다.

(그림 KSP 02.png, KSP 03.png 참조)

7. 에셋 번들을 생성한다.

메뉴 > Assets > Build AssetBundles 실행

Assets\AssetBundles 폴더에 notosanscjkkr-light.font 가 생성된 것을 확인할 수 있다.
