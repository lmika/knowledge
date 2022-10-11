---
title: DynamoDB JSON Attribute Types Quick Reference
type: reference
---

## Atomic Types

<table>
<thead>
<tr>
<th style="min-width:80px">Type</th>
<th style="min-width:80px">JSON</th>
<th>Value</th>
</tr>

</thead>
<tbody>
<tr>
<td>Binary</td>
<td><code>B</code></td>
<td>String value containing the Base64-encoded binary data.</td>
</tr>

<tr>
<td>Boolean</td>
<td><code>BOOL</code></td>
<td>Either <code>true</code> or <code>false</code></td>
</tr>

<tr>
<td>String</td>
<td><code>S</code></td>
<td>String value</td>
</tr>

<tr>
<td>Number</td>
<td><code>N</code></td>
<td>String with the numerical value</td>
</tr>

<tr>
<td>Null</td>
<td><code>NULL</code></td>
<td>Should always be <code>true</code></td>
</tr>
</tbody>
</table>

## Collection Types

<table>
<thead>
<tr>
<th style="min-width:80px">Type</th>
<th style="min-width:80px">JSON</th>
<th>Value</th>
</tr>
</thead>

<tbody>
<tr>
<td>List</td>
<td><code>L</code></td>
<td>A JSON array, with each element being an attribute with a type.</td>
</tr>

<tr>
<td>Map</td>
<td><code>M</code></td>
<td>A JSON object, with the keys being the map keys, and the values being an attribute with a type.</td>
</tr>
</tbody>
</table>

## Set Types

<table>
<thead>
<tr>
<th>Type</th>
<th>JSON</th>
<th>Value</th>
</tr>
</thead>

<tbody>
<tr>
<td>Binary Set</td>
<td><code>BS</code></td>
<td>A JSON array of Base-64-encoded binary data.</td>
</tr>

<tr>
<td>Number Set</td>
<td><code>NS</code></td>
<td>A JSON array of string with the numerical values.</td>
</tr>

<tr>
<td>String Set</td>
<td><code>SS</code></td>
<td>A JSON array of strings.</td>
</tr>
</tbody>
</table>

Sources:

- [AttributeValue API documentation](https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_AttributeValue.html): this the definitive guide from AWS.
- [DynamoDB Item size and format](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/CapacityUnitCalculations.html): more info about the particulars of each attribute type.