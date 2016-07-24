Mobile data analysis: can we predict users' demographic characteristics based on the patterns of app usage, geolocation, and mobile device properties?
======================================================================================================================================================

Research question
-----------------

The following research question will be answered in this report:

-   Can we predict users' demographic characteristics based on the
    patterns of app usage, geolocation, and mobile device properties?

Data
----

This analysis is part of Kaggle's challenge ["TalkingData Mobile User
Demographics"](https://www.kaggle.com/c/talkingdata-mobile-user-demographics)

The data of this project is composed of the following six files: -
gender\_age - events - phone.brand.device.model - app\_events -
app\_labels - label\_categories

### Descriptive analysis

**phone.brand.device.model table** has 187245 observations and 3
variables. Below are the numbers of unique values in each of the
variables in the table.

<table style="width:38%;">
<colgroup>
<col width="18%" />
<col width="19%" />
</colgroup>
<thead>
<tr class="header">
<th align="center">Variable</th>
<th align="center">Unique_value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center">device_id</td>
<td align="center">186716</td>
</tr>
<tr class="even">
<td align="center">phone_brand</td>
<td align="center">131</td>
</tr>
<tr class="odd">
<td align="center">device_model</td>
<td align="center">1598</td>
</tr>
</tbody>
</table>

It is worth noting that there are 529 duplicated values in device\_id
variable.

**gender\_age table** is connected with **phone.brand.device.model
table** through **device\_id variable**. This table has 74645
observations and 4 variables.

<table style="width:35%;">
<colgroup>
<col width="15%" />
<col width="19%" />
</colgroup>
<thead>
<tr class="header">
<th align="center">Variable</th>
<th align="center">Unique_value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center">device_id</td>
<td align="center">74645</td>
</tr>
<tr class="even">
<td align="center">gender</td>
<td align="center">2</td>
</tr>
<tr class="odd">
<td align="center">age</td>
<td align="center">85</td>
</tr>
<tr class="even">
<td align="center">group</td>
<td align="center">12</td>
</tr>
</tbody>
</table>

**events table** is connected with **phone.brand.device.model table**
through **device\_id variable**. This table has 3252950 observations and
5 variables.

<table style="width:35%;">
<colgroup>
<col width="15%" />
<col width="19%" />
</colgroup>
<thead>
<tr class="header">
<th align="center">Variable</th>
<th align="center">Unique_value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center">event_id</td>
<td align="center">3252950</td>
</tr>
<tr class="even">
<td align="center">device_id</td>
<td align="center">60865</td>
</tr>
<tr class="odd">
<td align="center">timestamp</td>
<td align="center">588125</td>
</tr>
<tr class="even">
<td align="center">longitude</td>
<td align="center">3588</td>
</tr>
<tr class="odd">
<td align="center">latitude</td>
<td align="center">3086</td>
</tr>
</tbody>
</table>

**app\_labels table** has 459943 observations and 2 variables.

<table style="width:35%;">
<colgroup>
<col width="15%" />
<col width="19%" />
</colgroup>
<thead>
<tr class="header">
<th align="center">Variable</th>
<th align="center">Unique_value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center">app_id</td>
<td align="center">113211</td>
</tr>
<tr class="even">
<td align="center">label_id</td>
<td align="center">507</td>
</tr>
</tbody>
</table>

**app\_events table** is connected with **events table** with
**event\_id variable** and **app\_labels table** with **app\_id
variable**. It has 32473067 observations and 4 variables.

<table style="width:38%;">
<colgroup>
<col width="18%" />
<col width="19%" />
</colgroup>
<thead>
<tr class="header">
<th align="center">Variable</th>
<th align="center">Unique_value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center">event_id</td>
<td align="center">1488096</td>
</tr>
<tr class="even">
<td align="center">app_id</td>
<td align="center">19237</td>
</tr>
<tr class="odd">
<td align="center">is_installed</td>
<td align="center">1</td>
</tr>
<tr class="even">
<td align="center">is_active</td>
<td align="center">2</td>
</tr>
</tbody>
</table>

**label\_categories table** is connected with **app\_labels table**. It
has 930 observations and 2 variables.

<table style="width:35%;">
<colgroup>
<col width="15%" />
<col width="19%" />
</colgroup>
<thead>
<tr class="header">
<th align="center">Variable</th>
<th align="center">Unique_value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center">label_id</td>
<td align="center">930</td>
</tr>
<tr class="even">
<td align="center">category</td>
<td align="center">836</td>
</tr>
</tbody>
</table>
