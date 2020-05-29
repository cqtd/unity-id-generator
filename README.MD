# ID Generator

### Install

OpenUPM으로 https://github.com/cqtd/unity-id-generator.git 설치



### Usage

```C#
public static class ID {
    static Worker _worker;
    public static long Generate() {
        if (_worker == null) _worker = new Worker(0,0);
        return worker.NextId();
    }
}

public class TestScripts : MonoBehaviour {

    public long InstanceId {get; protected set;}
    
    // How to call
    void Start() {
        InstancedId = ID.Generate();
    }
}
```

런타임의 인스턴스 ID 만들기에 적합

DB 관련 작업에 용이



### Reference

- Snowflake Unique ID Generator