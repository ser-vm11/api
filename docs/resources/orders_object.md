# ������ `Order`

��� | ��� | ��������
--- | --- | ---
id | string | ������������� ������
number | string | ����� ������
promoCode | string | ��������
status | [Order.Status](#status) | ������ ������
organization | [Order.Organization](#organization) | �����������, �������������� ���������
dates | [Order.Dates](#dates) | ���� ��������/���������� ������
editing | [Order.Editing](#editing) | ������������ �������������� ������
cost | [Order.Cost](#cost) | ���������
services | [[Order.Service](#service)] | ������ �����
 
#### ������ <a name="status">`Order.Status`</a>
 
��� | ��� | ��������
--- | --- | ------
message | string | ������� �������� �������
description | string | ������ �������� �������
isTaken | boolean | ����� ������
isGiven | boolean | ����� �����
isCanceled | boolean | ����� �������
isPaid | boolean | ����� �������
canUserRequestDriverCallback | boolean | ����������� ������� ������ �� ��������

#### ������ <a name="service">`Order.Service`</a>

� ����������� �� ���� ������, ������ ��� Order.Service ����� ��������� ��������� ����
 
##### ������ ���������������� ��������

��� | ��� | �������� | ��������
--- | --- | -------- | -------- 
type | string | ��� ������ | `shipping`
name | string | �������� ������ | `��������������� ��������`
sortIndex | number | ������ ���������� |
counteragents | object | �����������, ����������� � ������:
                         `payer` - ����������
                         `shipper` - �����������
                         `consignee` - ����������
                         `payer, shipper, consignee - ������� ���� [Counteragent](counteragent)
from | [Location](location) |  �������
to | [Location](location) | ����� �������
cargo | [Order.Cargo](#cargo) | ����������� ������� ������ �� ��������
cost | [Order.Service.Cost](#service.cost) | ����������� ������� ������ �� ��������