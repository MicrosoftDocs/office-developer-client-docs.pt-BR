---
title: Converter o código DAO em ADO
TOCTitle: Convert DAO code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 77d56efd63d6a0841b595f12456baa808751706e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720335"
---
# <a name="convert-dao-code-to-ado"></a>Converter o código DAO em ADO

**Aplica-se a**: Access 2013, o Office 2013

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
<th><p><strong>O ADO (ADODB)</strong></p></th>
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
<td><p>Recupera um conjunto de ponteiros para os registros no recordset.</p></td>
</tr>
<tr class="even">
<td><p>Snapshot-Type</p></td>
<td><p>Static</p></td>
<td><p>Recupera registros completos mas um recordset estático pode ser atualizado.</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>Keyset com opção adCmdTableDirect.</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Field</p></td>
<td><p>Field</p></td>
<td><p>Quando mencionado em um conjunto de registros.</p></td>
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
> Deslocamento do foco do registro atual por meio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sem usar primeiro o método **CancelUpdate** implicitamente executa o método **Update** .

### <a name="about-the-contributors"></a>Sobre os colaboradores

**Link fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com) . UtterAccess é o fórum principal de wiki e de ajuda do Microsoft Access.

- [Escolhendo entre o DAO e ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

