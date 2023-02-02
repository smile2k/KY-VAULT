# MVVM Overview
 
```ccard
type: folder_brief_live
```
 
---
%% Begin Waypoint %%
- **[[MVVM]]**

%% End Waypoint %%

---
LINK: https://learn.microsoft.com/en-us/dotnet/architecture/maui/mvvm

# 1. The MVVM pattern
There are three core components in the MVVM pattern: the model, the view, and the view model. Each serves a distinct purpose. The diagram below shows the relationships between the three components.
![[Pasted image 20230202091313.png]]

The benefits of using the MVVM pattern are as follows:
-   If an existing model implementation encapsulates existing business logic, it can be difficult or risky to change it. In this scenario, the view model acts as an adapter for the model classes and prevents you from making major changes to the model code.
-   Developers can create unit tests for the view model and the model, without using the view. The unit tests for the view model can exercise exactly the same functionality as used by the view.
-   The app UI can be redesigned without touching the view model and model code, provided that the view is implemented entirely in XAML or C#. Therefore, a new version of the view should work with the existing view model.
-   Designers and developers can work independently and concurrently on their components during development. Designers can focus on the view, while developers can work on the view model and model components.

The key to using MVVM effectively lies in understanding how to factor app code into the correct classes and how the classes interact.

# 2.View
- The view is responsible for defining the structure, layout, and appearance of what the user sees on screen. Ideally, each view is defined in XAML, with a limited code-behind that does not contain business logic. However, in some cases, the code-behind might contain UI logic that implements visual behavior that is difficult to express in XAML, such as animations.
(Chế độ xem chịu trách nhiệm xác định cấu trúc, bố cục và giao diện của những gì người dùng nhìn thấy trên màn hình. Lý tưởng nhất là mỗi chế độ xem được xác định trong XAML, với mã giới hạn phía sau không chứa logic nghiệp vụ. Tuy nhiên, trong một số trường hợp, mã phía sau có thể chứa logic giao diện người dùng thực hiện hành vi trực quan khó thể hiện trong XAML, chẳng hạn như hoạt ảnh.
)

# 3.View Model
- The view model implements properties and commands to which the view can data bind to, and notifies the view of any state changes through change notification events. The properties and commands that the view model provides define the functionality to be offered by the UI, but the view determines how that functionality is to be displayed.
 (Mô hình khung nhìn thực hiện các thuộc tính và lệnh mà khung nhìn có thể liên kết dữ liệu và thông báo cho khung nhìn về bất kỳ thay đổi trạng thái nào thông qua các sự kiện thông báo thay đổi. Các thuộc tính và lệnh mà mô hình khung nhìn cung cấp xác định chức năng được cung cấp bởi giao diện người dùng, nhưng khung nhìn xác định cách hiển thị chức năng đó.)
- In order for the view model to participate in two-way data binding with the view, its properties must raise the `PropertyChanged` event. View models satisfy this requirement by implementing the `INotifyPropertyChanged` interface, and raising the `PropertyChanged` event when a property is changed.
# 4.Model
- Model classes are non-visual classes that encapsulate the app's data. Therefore, the model can be thought of as representing the app's domain model, which usually includes a data model along with business and validation logic. Examples of model objects include data transfer objects (DTOs), Plain Old CLR Objects (POCOs), and generated entity and proxy objects.

 - Model classes are typically used in conjunction with services or repositories that encapsulate data access and caching.
# Connecting view models to views 
