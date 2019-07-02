事件bind
`This.event = this.event.bind(this)`
Function component vs class component

State 修改用setSate

生命周期

Props 和 state 都是状态数据，不一定是最后呈现的数据
他们的区别在于本component中会不会改变数据。
假如A会影响B，那么他们必须在一个总体的component下面，通过数据流下去。

Props 可以传递function，这样可以把子component的控制器完全做到它的父集
`<child event={this.event}/>`

state可以作为整体传递下去
`<child data={this.state}/>`

所有form 中的输入数据都需要设置一个 控制输入的function 不然无法输入
```
<input* name='stateName' onChange={this.handleChange}>
handleChange(event){
  const {name, value, type, checked} = event.target
  type === "checkbox"?
  this.setState({[name]:checked}):
  this.setState({[name]:value}):
}
```