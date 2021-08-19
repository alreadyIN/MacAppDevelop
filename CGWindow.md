#### 获取桌面上的窗口列表

```
NSMutableArray *windows = (NSMutableArray *)CGWindowListCopyWindowInfo(kCGWindowListOptionOnScreenOnly | kCGWindowListExcludeDesktopElements, kCGNullWindowID); 

for (NSDictionary *window in windows) { 
    NSString *owner = [window objectForKey:@"kCGWindowOwnerName" ]; 
    NSString *name = [window objectForKey:@"kCGWindowName" ]; 
    NSLog(@"%@ - %@",owner,name); 
} 
```
#### 可用键：

```
kCGWindowIsOnscreen 
kCGWindowLayer 
kCGWindowMemoryUsage 
kCGWindowName 
kCGWindowNumber 
kCGWindowOwnerName 
kCGWindowOwnerPID 
kCGWindowSharingState 
kCGWindowStoreType
```
