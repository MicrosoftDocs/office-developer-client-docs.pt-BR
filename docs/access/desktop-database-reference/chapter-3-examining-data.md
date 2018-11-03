---
title: 'Capítulo 3: Examinando dados'
TOCTitle: 'Chapter 3: Examining data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b489400536675fccced8f87aae515b019b87123
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936858"
---
# <a name="chapter-3-examining-data"></a>Capítulo 3: Examinando dados

**Aplica-se a**: Access 2013, o Office 2013

O capítulo 2 explicou como recuperar os dados de uma fonte de dados como um objeto **Recordset**. Este capítulo tratará do **Recordset** mais detalhadamente, incluindo como navegar por meio do **Recordset** e exibir os dados.

Os **Recordsets** têm métodos e propriedades criados para facilitar o movimento entre eles e examinar os conteúdos deles. Dependendo da funcionalidade oferecida pelo provedor, alguns métodos ou propriedades do **Recordset** poderão não estar disponíveis. Para continuar a exploração do objeto **Recordset**, considere um **Recordset** que será retornado pelo banco de dados de exemplo Northwind no Microsoft SQL Server 2000, usando o seguinte código:

```vb 
 
'BeginRsTour 
Public Sub RecordsetTour() 
 On Error GoTo ErrHandler: 
 
 Dim objRs As New ADODB.Recordset 
 Dim strSQL As String 
 
 strSQL = "SELECT ProductID, ProductName, UnitPrice FROM Products " & _ 
 "WHERE CategoryID = 7" '7 = Produce 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, _ 
 adLockReadOnly, adCmdText 
 
 'Clean up 
 objRs.Close 
 Set objRs = Nothing 
 Exit Sub 
 
ErrHandler: 
 If Not objRs Is Nothing Then 
 If objRs.State = adStateOpen Then objRs.Close 
 Set objRs = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndRsTour 
```

<br/>

Esta consulta SQL retorna um **Recordset** com cinco linhas (registros) e três colunas (campos). Os valores de cada linha são mostrados na tabela a seguir.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>CAMPO 0<br />
Nome = ProductID</p></th>
<th><p>CAMPO 1<br />
Nome = ProductName</p></th>
<th><p>CAMPO 2<br />
Nome = UnitPrice</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>7</p></td>
<td><p>Pêras secas orgânicas do Tio Bob</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="even">
<td><p>14</p></td>
<td><p>Tofu</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="odd">
<td><p>28</p></td>
<td><p>Chucrute Rssle</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="even">
<td><p>51</p></td>
<td><p>Maçãs secas Manjimup</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="odd">
<td><p>74</p></td>
<td><p>Tofu longa vida</p></td>
<td><p>10.0000</p></td>
</tr>
</tbody>
</table>


A próxima seção explica como localizar a posição atual do cursor neste **Recordset**de exemplo.

Este capítulo aborda os seguintes tópicos:

- [Localizando o registro atual (ADO)](locating-the-current-record.md)
- [Navegando nos dados (ADO)](navigating-through-the-data.md)
- [Noções básicas sobre a estrutura do Recordset (ADO)](understanding-recordset-structure.md)