### singularity
---
https://github.com/sylabs/singularity

http://getsingularity.com/

```go

import (
  "fmt"
  "os/exec"
  "strings"
  "testing"
)

func ImagePush(t *testing.T, cmdPath, imagePath, imgURI string) (string, []byte, error) {
  argv := []string{"push"}
  
  if imagePath != "" {
    argv = append(argv, imagePath)
  }
  
  argv = append(argv, imgURI)
  
  cmd := fmt.Sprintf("%s %s", cmdPath, strings.Join(argv, " "))
  out, err := exec.Command(cmdPath, argv...).CombinedOutput()
  
  return cmd, out, err
}
```

```
```

```
```


