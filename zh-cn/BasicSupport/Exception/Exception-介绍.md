[< 返回 BasicSupport 导航](../BasicSupport-导航.md)

本文建议阅读时间： 1 分钟。
> [!NOTE]
> 本文仅供参考，请以源码为准。

# `Exception`介绍
`Exception`提供了一个简单的异常类`Exception`。

`Exception`类属于`Xiaoxuan4096::Basic::Exception`命名空间。

`Exception`类部分代码使用了`<Windows.h>`。

以下是`Exception`类的成员变量。
```
private:
    std::wstring detail = L"Warning: An error occurred.";
    SYSTEMTIME time;
```
以下是`Exception`类的成员函数。这些函数**不会**抛出异常。
```
public:
    Exception(std::wstring exceptionDetail);
    std::wstring getExceptionDetail();
    SYSTEMTIME getExceptionTime();
```
如无特殊说明，函数类型默认为`void`。

---
## 创建`Exception`对象
使用`Exception(std::wstring exceptionDetail)`函数可以创建一个`Exception`对象。
> [!IMPORTANT]
> 这是一个**构造函数**。

|参数列表|类型|用途|
|---|---|---|
|exceptionDetail|`std::wstring`|存储异常的描述。需要手动指定。|

|涉及到的成员变量|类型|效果|
|---|---|---|
|detail|`std::wstring`|`exceptionDetail`的值被保存在这里。|
|time|`SYSTEMTIME`|当前系统时间被保存在这里。|

## 获取异常信息
使用`getExceptionDetail()`函数可以获取异常描述。

函数返回一个`std::wstring`对象，这个对象内存储了异常的描述。

使用`getExceptionTime()`函数可以获取异常发生的时间。

函数返回一个`SYSTEMTIME`对象，这个对象内存储了异常发生的时间。