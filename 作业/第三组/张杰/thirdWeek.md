#### 1.state��props���÷�������?
- propsһ�����ڸ�������������ͨ�ţ���Ҫ������������ݴ���
- stateһ����������ڲ������ݹ���
- props���÷�

```
    �����
    render() {
        var name = 'Alice';
        return <Profile name={name} />

    }
    �����
    render (){
        let name = this.props.name;
        return <div>{name}</div>

    }
```
- state���÷�

```
        constructor (){
            super();
            this.state = {
                val:'DefaultValue'
            }
        }
        updateData = (e) => {
            this.setState({
                val:e.target.value
            })
        }
        render(){
            return (
                <div>
                    <input type="text" onChange={this.updateData}/>
                    <h1>{this.state.val}</h1>
                </div>
            )
        }
```

#### 2.stateless component�Ķ�����е���ʲô��
- stateless:��״̬�����Ϊ������չʾ����������ݴ����props����չʾ
- stateless�ŵ㣺��ǿ��д����ķ����ԣ�����������Ⱦ����
- component���ڿ����У����Խ���ʾ�����ݷָ�ɲ�ͬ�������֮���ٽ���Щ�����ϵ�һ���������´�ʹ����ͬ�������ʱ��Ϳ��Ը���
- component�ŵ㣺����Ǿ����������ڵģ����������ǿ����оͿ��Ը���������Ҫ������д���

#### 3.дjsx�﷨,����ô������ʽ���ƺ�style��
- ͨ����ʽ�������룺

```
    <h1 style={titleStyle}>Hello World</h1>
```
- ����ͨ��import������ʽ�ļ�

```
    import './style.css'
```

#### 4.react render������ returnһ�������ʱ����Ҫע��ʲô?
- return ����ֻ����һ���պϵı�ǩ
- ���return�����ж�������ʱ����Ҫʹ�� () ���Ÿ�������

#### 5.react ��ô����һ������
```
    import React , { Component } from 'react'
```

#### 6.���ʵ������ӿڹ淶Լ����
- ʹ��propTypes
- �����Ǹ�Profile�������Ľ���ֵ�����˽ӿڹ淶

```
    Profile.propTypes = {
        url:PropTypes.string,
        name:PropTypes.string,
        id:PropTypes.number
    }
```

#### 7.��ô�������Ĭ�ϲ���
- ʹ��defaultProps

```
    Profile.defaultProps = {      
        name:'xxx',
        id:0,
        url:''
    };
```

#### 8.ref��ʲô?��ô��ȡref��Ӧ��ʵ��
- ref��React�е�һ�����ԣ���render��������ĳ�������ʵ��ʱ�����Ը�render�е�ĳ������DOM�ڵ����һ��ref���ԣ�ͨ��ref���ԣ����ǻ������õ�������DOM��Ӧ����ʵDOM�ڵ�
- ���������ַ�ʽ���Ի�ȡref��Ӧ��ʵ��

```
    <input type="text" ref="username" />  
       
    var usernameDOM = this.refs.username.getDOMNode();  
    var usernameDOM = React.findDOMNode(this.refs.username); 
```

#### 9.react��ô��ȡDOM�ڵ�
- ����ͨ��ref��ȡ����Ӧ��DOM�ڵ�
- ͨ��this.props.children��ȡ���������DOM�ڵ�

#### 10.react�Ƴ��ڵ�������������ĸ�?
- ����Ⱦ֮ǰ ```return false```
- ʹ�����·�ʽ����ɾ�����Ӹ��ڵ�ɾ��

``` 
    ReactDOM.unmountComponentAtNode(document.getElementById('app'));
```
