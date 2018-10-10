---
title: Converter o código DAO em ADO
TOCTitle: Converting DAO Code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7039d9322956e4fcbca4081eff75868ccf306e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461975"
---
# <a name="converting-dao-code-to-ado"></a>Converter o código DAO em ADO

**Aplica-se a**: Access 2013 | Office 2013

> [!NOTE]
> Versões da biblioteca DAO anteriores à versão 3.6 não são fornecidas ou são suportadas no Access.

## <a name="dao-to-ado-object-map"></a>DAO para mapa de objeto ADO

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><strong>DAO</strong></p></th>
<th><p><strong>ADO(ADODB)</strong></p></th>
<th><p><strong>Observação</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBEngine</p></td>
<td><p>Nenhuma</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Workspace</p></td>
<td><p>Nenhuma</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Banco de dados</p></td>
<td><p>Connection</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Recordset</p></td>
<td><p>Recordset</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Dynaset-Type</p></td>
<td><p>Keyset</p></td>
<td><p>Recupera um conjunto de ponteiros para os registros no conjunto de registros</p></td>
</tr>
<tr class="even">
<td><p>Snapshot-Type</p></td>
<td><p>Static</p></td>
<td><p>Recupera registros completos mas um conjunto de registros Static não pode ser atualizado.</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>Keyset com opção adCmdTableDirect</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Field</p></td>
<td><p>Field</p></td>
<td><p>Quando mencionado em um conjunto de registros</p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a>DAO

#### <a name="open-a-recordset"></a>Abrir um Recordset

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a>Editar um Recordset

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a>ADO

#### <a name="open-a-recordset"></a>Abrir um Recordset

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a>Editar um Recordset

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> O deslocamento do foco do registro atual por meio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sem usar primeiro o método **CancelUpdate** executará implicitamente o método **Update**.

### <a name="about-the-contributors"></a>Sobre os colaboradores

**Link fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com) . UtterAccess é o fórum principal de wiki e a Ajuda do Microsoft Access.

- [Escolhendo entre o DAO e ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)



