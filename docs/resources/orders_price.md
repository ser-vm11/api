# ��������� ������

`GET https://api.vozovoz.ru/v1/orders/[ID]`

��������� �������:

��� | ��� | ��������
--- | --- | ---
id | string | ������������� ������
services | [Order.Service](orders_object#service) | ����� ������
promoCode | string | ��������
save | boolean[Order.Status](#status) | ������ ������
organization | [Order.Organization](#organization) | �����������, �������������� ���������
dates | [Order.Dates](#dates) | ���� ��������/���������� ������
editing | [Order.Editing](#editing) | ������������ �������������� ������
cost | [Order.Cost](#cost) | ���������
services | [Order.Services](#services) | ������ �����

����������:

```js
HTTP/1.1 200 OK
{
    "data" : [������ Order](order_object)
}
```