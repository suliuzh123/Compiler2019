## 实验2 语义分析

1. **截止日期**: ~~提交日期暂定2019年11月4日 19:59:59 周一晚之前, 根据课堂上课进度可能会适当调整~~2019年11月8日 23:59:59 周五晚之前提交

2. 与实验一不同的是，实验二不再借助已有的工具，所有的任务都必须手写代码来完成, 新增代码量大约在 600-800 行左右.
    - 实验二任务较为细致、琐碎, 尽可能对每个产生式设置一个处理函数.
    - 实验二是在实验一的基础基本上不需要对原有的程序进行大量修改，进行适当扩展就可；
    - 后续的实验三中还会用到本次实验已经写好的代码, 并会对本次实验中的每个函数进行大量修改和扩充，请系统地设计代码结构和各模块之间的接口；

3. 代码部分文件结构，仅供参考
```
./Code
├── lexical.l   # Lab1 词法正则
├── syntax.y    # Lab1 文法
├── main.c      # 入口函数
├── Makefile    # 原始Makefile
├── node.c      # Lab1 语法分析: 语法树建立和打印输出
├── node.h
├── semantic.c  # Lab2 语义分析: 在语法树的基础上进行符号表操作和语义分析
├── semantic.h
└──
```

4. `main.c` 部分代码, 仅供参考
```c
int main(int argc, char** argv){
    if (argc <= 1){
        return 1;
    }
    FILE* fp = fopen(argv[1],"r");
    if (!fp){
        perror(argv[1]);
        return 1;
    }
    yylineno=1;
    yyrestart(fp);
    yyparse();
    if(errorNum == 0){
        initHashtable();
        traverseTree(Root);
    }
    return 0;
}
```

5. Makefile文件在编写和测试代码中可自行测试修改, 但最终提交时请务必通过原始Makefile的编译, 对提交的代码文件最终会用原始Makefile进行测试




