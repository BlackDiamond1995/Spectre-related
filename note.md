### 术语
- BTB: Branch Target Buffer
    - 用于存储分支指令上一次执行中得到的下一条指令地址
    - 一般情况，BTB表只会保存source instruction保存低31bit的跳转记录，即如果它记录了0x4141.0004.1000 to 0x4141.0004.5123，那么也会应用到0x4242.0004.1000
    - 对于Indirect Branch，source instruction只存储12bit，但是尚未清楚是哪12bit，还有相应的BHB状态
- RSB: Return Stack Buffer
    -  store the 𝑁 most recent return addresses
- ROB: Redorder Buffer
    - 乱序执行时，暂存未定指令的执行结果
    - on Intel’s Skylake has space for 224 micro-ops, or about 200 instructions for typical code
- BHB: Branch History Buffer
    - 存储最近29次branch
- 上述表是进程无关的

### 杂项
- Instructions can be executed out of order, but must always retire in order.
- BTB表之后

### 想法
- 编译器增加新的关键字，用于标识敏感数据，保护在特定区域
- 将现有保护机制综合起来，根据实际情况由编译器自动选择机制