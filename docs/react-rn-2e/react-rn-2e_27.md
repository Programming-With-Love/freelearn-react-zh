# 第二十七章：测试你的知识答案

# 第一章

1.  声明式 UI 结构是什么，React 如何支持这个想法？

1.  **声明式 UI 结构定义了 UI 组件是什么，而不是担心它是如何定义的。React 通过允许使用 JSX 语法声明组件来支持这个想法。**

1.  React 如何提高渲染性能？

1.  **React 具有虚拟 DOM，它比较内存中组件数据的更改，尽量避免浏览器 DOM。React 16 具有新的内部架构，允许将渲染分成更小的工作块并优先处理。**

1.  何时会渲染片段？

1.  **片段用于避免渲染不必要的 DOM 元素**

# 第二章

1.  您可以将所有标准 HTML 标签用作 JSX 元素吗？

1.  **是的，React 默认支持这一点**

1.  如何从组件中访问子元素？

1.  **通过 `children` 属性始终可以访问子 JSX 元素**

1.  React 中的 `Fragment` 组件是做什么的？

1.  **它作为一个容器组件，通过 否定 渲染无意义的元素， 如 容器 divs**

# 第三章

1.  为什么总是初始化组件的状态是一个好主意？

1.  **因为如果 `render()` 方法期望状态值，您需要确保它们始终存在，以避免意外的渲染行为。**

1.  何时应该使用属性而不是状态？

1.  **状态应该只用于可以改变的值。对于其他所有情况，应该使用属性。**

1.  在 React 中什么是上下文？

1.  **上下文用于避免瞬态属性。上下文用于与少数组件共享常见数据。**

# 第四章

1.  在 React 中，事件处理程序是什么使得它声明式的？

1.  **React 事件处理程序被声明为组件 JSX 的一部分**

1.  高阶事件处理程序函数的常见用途是什么？

1.  **当您有多个处理相同事件的组件时，可以使用高阶函数将被点击的项目的 ID 绑定到处理程序函数**

1.  您可以将内联函数传递给事件属性吗？

1.  **是的。当事件处理程序很简单时，这是更可取的。**

1.  为什么 React 使用事件实例池而不是在每个事件中创建新实例？

1.  **为了避免在 短时间内 触发大量事件时调用垃圾收集器来删除未使用的事件实例**

# 第五章

1.  为什么应该避免庞大的 React 组件？

1.  **因为它们难以理解，并且难以重构为以后可重用的较小组件。**

1.  为什么应该使组件功能化？

1.  **功能组件只依赖于传递给它的属性值。它们不依赖于状态或生命周期方法，这两者都是潜在的问题来源。**

1.  渲染道具如何简化 React 应用程序？

1.  **它们减少了组件的直接依赖数量，使您能够组合新的行为。**

# 第六章

1.  `render()`是一个生命周期方法吗？

1.  **是的，`render()`与任何其他生命周期方法没有区别。**

1.  以下哪项是`componentWillUnmount()`方法的有效用途？

1.  **取消异步操作，如果组件未挂载则会失败。**

1.  错误边界组件使用哪个生命周期方法？

1.  `**componentDidCatch()**`

# 第七章

1.  以下哪项最能描述`prop-types`包？

1.  **用于在开发过程中验证传递给组件的属性值。**

1.  如何验证属性值是否可以被渲染？

1.  **使用`PropTypes.node`验证器。**

1.  `PropTypes.shape`验证器的目的是什么？

1.  **确保对象具有特定类型的特定属性，忽略任何额外的属性。**

# 第八章

1.  何时应该继承组件状态？

1.  **只有当你有许多不同的组件都共享相同的状态结构，但渲染不同的输出时**

1.  什么是高阶组件？

1.  **返回另一个组件的组件**

1.  如果你从一个组件继承 JSX，你应该覆盖什么？

1.  **你可以在`componentDidMount()`中向继承的组件传递新的状态值。**

# 第九章

1.  `react-router`包是 React 应用程序中路由的官方包，因此是唯一的选择。

1.  **不，`react-router`是 React 的事实上的路由解决方案，除非你有充分的理由不使用它。**

1.  `Route`和`Router`组件之间有什么区别？

1.  **`Route`用于根据 URL 匹配渲染组件，`Router`用于声明路由-组件映射。**

1.  如何在路由更改时仅更改 UI 的某些部分？

1.  **您可以使用`Route`组件根据提供的`path`属性渲染特定于任何给定部分的内容。您可以有多个具有相同`path`值的`Route`。**

1.  何时应该使用`NavLink`组件？

1.  **当您想要使用`activeStyle`或`activeClassName`属性来为活动链接设置样式时**

1.  如何从 URL 路径中获取值？

1.  **您可以使用`: `语法来指定这是一个变量，`react-router`将将此值作为属性传递给您的组件**

# 第十章

1.  `react-dom`中的`render()`函数和`react-dom/server`中的`renderToString()`函数之间有什么区别？

1.  **`render()`函数仅用于在浏览器中将 React 组件内容与 DOM 同步。`renderToString()`函数不需要 DOM，因为它将标记呈现为字符串。**

1.  服务器端的路由是必要的，因为：

1.  **服务器上的路由将根据请求的 URL 确定渲染的内容。然后将此内容发送到浏览器，以便用户感知更快的加载时间。**

1.  在协调服务器端渲染的 React 标记与浏览器中的 React 组件时应该使用哪个函数？

1.  **当服务器发送渲染的 React 组件时，始终使用`hydrate()`。与`render()`不同，`hydrate()`期望渲染的组件标记并且可以有效地处理它。**

# 第十一章

1.  为什么 React 开发人员应该考虑移动优先的方法来设计他们的应用程序？

1.  **因为将移动设备作为应用程序的主要显示目标可以确保您可以处理移动设备，并且向更大的设备进行扩展比反之容易。**

1.  `react-router`与`react-bootstrap`集成良好吗？

1.  **是的。尽管您可能希望使用`react-router-bootstrap`包，以确保您可以将链接添加到`NavItem`和`MenuItem`组件中。**

1.  如何使用`react-bootstrap`渲染项目列表？

1.  使用`react-bootstrap`中的`ListGroup`和`ListGroupItem`组件。

1.  为什么应该为`react-bootstrap`表单组件创建一个抽象？

1.  **因为有许多相关的组件需要用于基本输入，创建这种抽象会让生活更容易。**

# 第十二章

1.  React Native 的主要目标是什么？

1.  **让 React 开发人员能够将他们已经了解的构建 UI 组件的知识应用到构建原生移动应用程序中。**

1.  React Native 在 iOS 和 Android 上提供完全相同的体验吗？

1.  **不，iOS 和 Android 有根本不同的用户体验。**

1.  React Native 是否消除了移动 Web 应用的需求？

1.  **不，移动 Web 应用程序始终需要。当您需要原生移动应用程序时，React Native 就在那里为您。**

# 第十三章

1.  **`create-react-native-app`**工具是由 Facebook 创建的

1.  **不，这是一个社区支持的工具，跟随** `create-react-app` **的脚步**

1.  为什么应该全局安装**`create-react-native-app`**？

1.  **因为这是一个用于生成项目样板的工具，实际上并不是项目的一部分**

1.  Expo 应用在移动设备上的作用是什么？

1.  **这是一个帮助开发人员在开发过程中在移动设备上运行其应用程序的工具，开销非常小**

1.  React Native 打包程序能够模拟 iOS 和 Android 设备

1.  **它不会这样做，但它会与 iOS 和 Android 模拟器通信以运行应用程序**

# 第十四章

1.  CSS 样式和 React Native 组件使用的样式有什么区别？

1.  **React Native 与 CSS 共享许多样式属性。样式属性在 React Native 中表示为普通对象属性**

1.  为什么在设计布局时需要考虑状态栏？

1.  **因为状态栏可能会干扰 iOS 上的组件**

1.  什么是 flexbox 模型？

1.  **flexbox 布局模型用于以一种抽象许多细节并自动对布局更改做出灵活响应的方式来布局组件**

1.  在考虑布局选项时，屏幕方向是否是一个因素？

1.  **是的，在开发过程中，始终需要确保在纵向或横向方向上没有意外情况**

# 第十五章

1.  在 React web 应用和 React Native 应用中导航的主要区别是什么？

1.  **Web 应用程序依赖于 URL 作为移动的中心概念。原生应用程序没有这样的概念，因此由开发人员和他们使用的导航库来管理他们的屏幕。**

1.  应该使用什么函数来导航到新屏幕？

1.  **屏幕组件会传递一个导航属性。您应该** **使用** `navigation.navigate()` **来移动到另一个屏幕。**

1.  react-navigation 是否为您处理返回按钮功能？

1.  **是的。包括 Android 系统上的内置返回按钮。**

1.  如何将数据传递给屏幕？

1.  **您可以将普通对象作为第二个参数传递给** `navigation.navigate()`。 **然后，通过** `navigation.getParam()` **可以访问这些属性。**

# 第十六章

1.  **`FlatList`**组件可以呈现什么类型的数据？

1.  **`FlatList`期望一个对象数组。`renderItem`属性接受一个负责渲染每个项目的函数。**

1.  为什么`key`属性是传递给`FlatList`的每个数据项的要求？

1.  **这样列表可以进行有效的相等性检查，有助于在列表数据更新期间提高渲染性能。**

1.  如何渲染在滚动期间保持固定位置的列表控件？

1.  **您可以使用`FlatList`的`ListHeaderComponent`属性。**

1.  当用户滚动列表时，如何懒加载更多数据？

1.  **您可以为`FlatList`的`onEndReached`属性提供一个函数。当用户接近列表的末尾时，将调用此函数，并且该函数可以使用更多数据填充列表数据。**

# 第十七章

1.  进度条和活动指示器有什么区别？

1.  **进度条是确定的，而进度指示器用于指示不确定的时间量。**

1.  React Native 的`ActivityIndicator`组件在 iOS 和 Android 上是否工作相同？

1.  **是的，这个组件是平台无关的。**

1.  如何以平台无关的方式使用`ProgressViewIOS`和`ProgressBarAndroid`组件？

1.  **您可以定义自己的`ProgressBar`组件，导入具有特定于平台的文件扩展名的其他组件。**

# 第十八章

1.  在 React Native 中找到的地理位置 API 的工作方式与 Web 浏览器中找到的地理位置 API 相同。

1.  **是的，它是相同的 API。**

1.  React Native 应用程序中地理位置 API 的主要目的是什么？

1.  **查找设备的纬度和经度坐标，并将这些值与其他 API 一起使用，以查找有用信息，比如地址。**

1.  `MapView`组件能够显示用户附近的兴趣点吗？

1.  **是的，默认情况下已启用。**

1.  如何在地图上标记点？

1.  **通过将纬度/经度数组数据作为属性传递给`MapView`组件。**

# 第十九章

1.  为什么要更改文本输入的虚拟键盘上的返回键？

1.  **因为在某些情况下，有一个搜索按钮或其他更符合输入上下文的东西是有意义的**

1.  应该使用哪个`TextInput`属性将输入标记为密码字段？

1.  `**secureTextEntry**`

1.  为什么要为选择元素创建抽象？

1.  **由于两个平台之间的样式挑战**

1.  为什么要为日期和时间选择器创建抽象？

1.  **因为 iOS 和 Android 的组件完全不同**

# 第二十章

1.  警报和模态之间有什么区别？

1.  警报在继承移动环境的外观和感觉方面做得很好，而模态是常规的 React Native 视图，您可以完全控制其样式。

1.  哪个 React Native 组件可用于创建覆盖屏幕上其他组件的模态视图？

1.  `Modal`组件。

1.  在 Android 系统上显示被动通知的最佳方法是什么？

1.  您可以使用`ToastAndroid` React Native API。在 iOS 上没有不涉及自己编写代码的好的替代方法。

1.  React Native Alert API 仅在 iOS 上可用。

1.  错误

# 第二十一章

1.  Web 应用程序和本机移动应用程序之间用户交互的主要区别是什么？

1.  没有鼠标。相反，用户使用手指与您的 UI 进行交互。这是一种根本不同于使用鼠标的体验，需要进行调整。

1.  如何在 React Native 中为用户提供触摸反馈？

1.  通过使用`TouchableOpacity`或`TouchableHighlight`组件包装可触摸组件。

1.  移动应用程序中的滚动比 Web 应用程序中的滚动复杂得多的原因是什么？

1.  在移动 Web 应用程序中滚动需要考虑诸如速度之类的因素，因为用户是用手指进行交互的。否则，交互会感觉不自然。

1.  为什么要使用`ScrollView`组件来实现可滑动行为？

1.  因为这是用户在移动 Web 应用程序中习惯的，以及他们学习 UI 控件的方式。

# 第二十二章

1.  `Image`组件的`source`属性接受哪些类型的值？

1.  图像组件接受本地文件和远程图像 URL 的路径。

1.  在图像加载时应该使用什么作为占位符？

1.  您应该使用在图像使用的上下文中有意义的占位图像。

1.  如何使用`Image`组件缩放图像？

1.  通过设置`width`和`height`属性，`Image`组件将自动处理图像的缩放。

1.  安装`react-native-vector-icons`包值得吗？

1.  是的，这个包为您的应用程序提供了数千个图标，并且图标是向用户传达意图的重要工具。

# 第二十三章

1.  为什么`AsyncStorage` API 中的操作是异步的？

1.  为了避免干扰 UI 的响应性。

1.  您会使用哪个`AsyncStorage` API 来一次查找多个项目？

1.  `AsyncStorage.getAllKeys()`和`AsyncStorage.multiGet()`的组合。

1.  在 React Native 应用程序中，如何获取设备的连接状态？

1.  您调用`NetInfo.getConnectionInfo()`并读取生成的连接类型。

1.  在 React Native 应用程序中如何响应连接状态的变化？

1.  您可以通过调用`NetInfo.addEventListener('connectionChange', ...)`来监听`connectionChange`事件。

# 第二十四章

1.  以下哪项最能描述 Flux？

1.  Flux 是一种用于控制应用程序中数据单向流动的架构模式，使变化更加可预测。

1.  Flux 和 Redux 之间有什么区别？

1.  Redux 是 Flux 概念的一种有偏见的实现，您可以使用它来帮助管理应用程序中的数据流。

1.  如何将 Redux 存储中的数据传递到您的组件中？

1.  您使用`connect()`高阶函数将您的组件连接到存储，使用一个将存储数据转换为组件属性的函数。

1.  Redux 在 Web 应用程序和原生移动应用程序中有什么区别？

1.  没有区别。

# 第二十五章

1.  Relay 和其他受 Flux 启发的库（如 Redux）之间有什么区别？

1.  Relay 通过允许数据依赖声明并隐藏所有服务器通信复杂性来帮助扩展您的 Flux 架构。

1.  Relay 如何简化 React 组件的数据需求？

1.  通过合并数据依赖查询，您可以准确地看到您的组件使用的所有数据，而无需查看执行获取操作的代码。

1.  在基于 Relay 的应用程序中，您的 React 组件如何与服务器通信？

1.  Relay 编译在您的组件中找到的 GraphQL 查询，并为您处理所有的 GraphQL 服务器通信，包括缓存优化。