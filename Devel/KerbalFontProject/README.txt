
�ҽ��ڵ�� �Ʒ� ����Ʈ���� �����Խ��ϴ�.
from https://github.com/sarbian/KerbalFontProject



�ѱ���Ʈ ��������� �Ʒ��� �����ϴ�.

1. unity 5.2.x ���� ��ġ(�ݵ�� 5.4 ���� ������ ��ġ�ؾ� �Ѵ�.)

2. unity �� �����ϰ� �� ������Ʈ�� �����Ѵ�.

3. Assets ������ �Ʒ� ������ �����Ѵ�.

 - Assets\AssetBundles
 - Assets\Editor
 - Assets\Fonts
 - Assets\Resources
 - Assets\Resources\Fonts & Materials

4. ��Ʈ�� �߰��Ѵ�.

Assets\Fonts ������ NotoSansCJKkr-Light.otf �� ������ �ִ´�.
Assets ������ KS1001.txt �� ������ �ִ´�.

5. ���¹��� ���� ��ũ��Ʈ �߰�

Assets\Editor �� CreateAssetBundles.cs �� �����Ѵ�.
������ �Ʒ��� ����.

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

4. Text Mesh Pro ��ġ

5. ��Ʈ ���� ���� �� ����

�޴� > Window > TextMeshPro - Font Asset Creator ����

Assets\Resources\Fonts & Materials �ô��� ������ NotoSansCJKkr-Light SDF.asset �� �־��ش�.

6. ���� ���� ������ �ش�.

(�׸� KSP 02.png, KSP 03.png ����)

7. ���� ������ �����Ѵ�.

�޴� > Assets > Build AssetBundles ����

Assets\AssetBundles ������ notosanscjkkr-light.font �� ������ ���� Ȯ���� �� �ִ�.
