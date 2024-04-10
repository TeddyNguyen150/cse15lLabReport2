```
Current directory
$ pwd
/workspaces/lecture1
```

```
1. cd no arguments: changes current directory to home
@TeddyNguyen150 ➜ /workspaces $ cd
@TeddyNguyen150 ➜ ~ $

2. cd directory: changes current directory to wanted directory
@TeddyNguyen150 ➜ /workspaces $ cd lecture1/
@TeddyNguyen150 ➜ /workspaces/lecture1 (main) $

3. cd file: does nothing, cannot change directory to a file
@TeddyNguyen150 ➜ /workspaces/lecture1 (main) $ cd Hello.java
bash: cd: Hello.java: Not a directory
```

```
1. ls no arguments: lists current directory's children
@TeddyNguyen150 ➜ /workspaces/lecture1 (main) $ ls
Hello.java  README  messages

2. ls directory: lists wanted directory's children
@TeddyNguyen150 ➜ /workspaces/lecture1 (main) $ ls messages
en-us.txt  es-mx.txt  zh-cn.txt

3. ls file: lists the file
@TeddyNguyen150 ➜ /workspaces/lecture1 (main) $ ls Hello.java
Hello.java
```

```
1. cat no arguments: infinite loop
@TeddyNguyen150 ➜ /workspaces/lecture1 (main) $ cat
^C

2. cat directory: does nothing, cannot cat a directory
@TeddyNguyen150 ➜ /workspaces/lecture1 (main) $ cat messages/
cat: messages/: Is a directory

3. cat file: prints the contents of the file
@TeddyNguyen150 ➜ /workspaces/lecture1 (main) $ cat Hello.java 
import java.io.IOException;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;

public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
    System.out.println(content);
  }
```
