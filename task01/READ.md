# task 1_1

**����ǩlabel**
labelԪ�ؼ�����Ҫ����Ϊ�����԰�����ӽṹ�����ӱ��Ŀ����ԺͿɷ����ԡ�
���Ԫ��������ÿ����Ԫ�������������������Ա�ǩ�������������У�����Ԫ�ر�ǩ������������ı�Ԫ�ػ�ý��㡣
```
/*��ʽ��*/
<label>email<input name="email" type="text"></lable>
```
����
```
/*��ʽ��*/
<lable for="author">Name:</lable>
<input name="author" id="author" type="text">
/*<label>��ǩ��for����Ӧ�������Ԫ�ص�id������ͬ��*/
```

# task 1_2

���Ļ��߶��뻹�������(�s���t )

# task 1_3
���ַ���������

1. �������ҷ�ʽ���ӣ�Ȼ��ȫ��`float: left;`�����ú��м���ӵ���߾ࡣ

2. ʹ��flex���Բ��֣�ע�������м����`flex��1��`����Ȼ�ܿ���ѹ���������ӵĿ�ȡ�

3. ���߾಼�֣�˫�������ʥ������

# task_1_4
## 1.1 ˮƽ����
### 1.1.1 ����Ԫ��
ֻ��Ҫ������Ԫ�ذ�����һ������displayΪblock�ĸ���Ԫ���У��ٸ���Ԫ������ `text-align:center`
> ����Ԫ�أ����֣����ӣ���������inline����inline-*����Ԫ�أ�inline-block��inline-table��inline-flex��

### 1.1.2 ��״Ԫ��
- �����״Ԫ��
���á�����margin��ֵΪ��auto����ʵ�־���
- �������״Ԫ��
1. ���� table ��ǩ������margin:auto
2. ���� `display;inline` ��Ȼ��ʹ�� `text-align: center`
3. ���� `position:relative` �� `left:50%`������Ԫ������float�� `position:relative` ��` left:50%`����Ԫ������ `position:relative` �� `left:-50%`
4. ʹ��flexbox���֣�ֻ��Ҫ�Ѵ�����Ŀ�״Ԫ�صĸ�Ԫ���������`display:flex`��`justify-content:center`����

## 1.2 ��ֱ����
###1.2.1 ��Ԫ�ظ߶�ȷ���ĵ����ı�
���ø�Ԫ�ص� height �� line-height �߶�һ�¡�

###1.2.2 ��Ԫ�ظ߶�ȷ���Ķ����ı�
1.���� table (����tbody��tr��td)��ǩ��ͬʱ���� vertical-align��middle
2.�� chrome��firefox �� IE8 ���ϵ�������¿������ÿ鼶Ԫ�ص� display Ϊ table-cell������ vertical-align ����
###1.2.3 ��֪�߶ȵĿ�״Ԫ�ؽ������
```
.item{
  top: 50%;
  margin-top: -50px;
  position: absolute;
  padding:0;
}
```
> ������div���Ͻ���ҳ�涨λ������Ҫ���ư��div��С


##1.3 ˮƽ��ֱ����
###1.3.1  ��֪�߶ȺͿ�ȵ�Ԫ�ؽ������
����Ԫ�ض�λΪabsolute����������top, left����ֵΪ50%��margin-top��margin-leftΪԪ�ظ߶�һ��ĸ�ֵ���ɡ�
```
.item{
   position: absolute;
   top: 50%;
   left: 50%;
   margin-top: -75px;
   margin-left: -75px;
  }
```
###1.3.2 δ֪�߶ȺͿ��Ԫ�ؽ������
ʹ�����Ƶ�transform���������壬����ʵ�֡�
```
.item{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

###1.3.3 ʹ��flex����ʵ��
```
.parent{
  display: flex;
  justify-content:center;
  align-items: center;
  /* ע��������Ҫ���ø߶����鿴��ֱ����Ч�� */
  background: #AAA;
  height: 300px;
}
```

## 1.4 ���Ըı�display����
��һ����Ȥ��������ǵ�ΪԪ�أ�����֮ǰ��ʲô����Ԫ�أ�display:none ���⣩�������� 2 ����֮һ��
1. `position : absolute`
2. `float : left` �� `float:right`
Ԫ�ػ��Զ���Ϊ�� `display:inline-block` �ķ�ʽ��ʾ����Ȼ�Ϳ�������Ԫ�ص� width �� height ����Ĭ�Ͽ�Ȳ�ռ����Ԫ�ء�

## ����
1. ��һ��ʹ�þ��Զ�λ���еķ���
��������֪����Ȼ�߶ȵ�Ԫ��
![](http://images.cnitblog.com/blog/130623/201310/28171709-bbe4bd7ad1af4171b4be67d452743748.png)

2. ʹ�ø��������Զ�λ������ˮƽ����
�˷���Ҳ�ǹ��ڸ���Ԫ����ôˮƽ���еĽ���������������ǲ���Ҫ֪����Ҫ���е�Ԫ�صĿ�ȡ���1.1.2�ĵ�3��
