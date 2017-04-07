{{ self.title() }}

## ��������

�����ӱ��ⶼ���ӷ����� `����` �ˡ�

**Ҫǿ���Ķ���**��ôд��

���ڵĹ�ʽ��$sin \left(a x + b \right)$��

�м�Ĺ�ʽ��
$$
\frac{-b\pm\sqrt{b^2-4ac}}{2a}
$$

1. ��һ��
2. �ڶ���

* ��һ��
* �ڶ���

�ַ�������� `This is a string`

```
int main(int argc, char** argv);
```

��Ҫ��markdown�Դ����﷨����ͼƬ����ΪĿǰ֧�ֲ��ã����������﷨����ͼƬ��

{{ render("template('image', resource = resource('3.jpg'), size = 0.5, align = 'middle', inline = False)") }}

���� `inline` Ϊ `False` ��ʾ����һ����ռһ�е�ͼƬ����ʱ֧�� `align`��ѡ��Ϊ `left`��`middle` �� `right`��

ͼƬ��Ҫ����������Ŀ¼�� `resources` ��Ŀ¼�¡�

����б����߲����ṩ�Ĺ��ܣ���Ҫֱ��ʹ�� tex �� html ����ģ���ʹ�����з�ʽ��������һ�ָ�ʽ�³���

{{ render("'\\clearpage'", 'noi') }}

{{ render(''' '<a href="http://oj.thusaac.org">TUOJ</a>' ''', 'html') }}

������һ��������Ϊ���Ű�ÿ�ǿ�м���һ����ҳ������˼������ `noi` ��ʾֻ������ NOI ��������ʱ��ʹ��������ڶ����������������κ� html ��ʽ��Ŀ��ʱ�����һ����棨����

��ѡ�Ĳ����� `html`��`tex`��`noi`��`uoj`��`ccpc`��`ccc`��`tuoj`��`ccc-tex`��`ccc-html`��`tuoj-tex`��`tuoj-html`��

## �����ʽ

{{ self.input_file() }}

�������ݾ�������⻷��˵���������ļ����Ǳ�׼����ȡ�

�����һ�а���һ�������� $n$����֤ $n \le {{ tools.hn(prob.args['n']) }}$������������ `conf.json` �е� `args` �� `n` �Ȼ���á��ÿ����ĸ�ʽ���������ʱ�ȿ��� `['args']` Ҳ���� `.args`�����ÿ����ĸ�ʽ�� `$10^9$`��`1,000,000,007`��

## �����ʽ

{{ self.output_file() }}

�������Զ��������� `1.in/ans` Ȼ����Ⱦ�������У����ֻ��һ����������ȥ��ǰ���У�������Ȼ����� `1.in/ans`������ `1` �������ַ�����

{% set vars = {} -%}
{%- do vars.__setitem__('sample_id', 1) -%}
{{ self.sample_text() }}

������ֻ��ʾ���ڵڶ���������������Ⱦ�������С�

{% do vars.__setitem__('sample_id', 2) -%}
{{ self.sample_file() }}

## ������

ͬ����������markdownԭ���ı��ʹ�����з�ʽ��Ⱦһ��������б����������Ŀ¼�� `tables` ��Ŀ¼�¡�

{{ render("table('data')") }}

{{ render("table('table', {'width' : [1, 6]})") }}

�������Ӽ� `oi_tools/sample/tables`��ԭ������һ����ά��json���洢��`null` ��ʾ����һ�кϲ�����֧�ֺ���ϲ���������jinja�ĸ�ʽд���������е� `data.json`���������Ը����������ɣ��������޹صı��������� `table.json` �����洢��
