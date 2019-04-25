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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295517"
---
# <a name="convert-dao-code-to-ado"></a>Converter o código DAO em ADO

**Aplica-se ao**: Access 2013, Office 2013

> [!NOTE]
> As versões da biblioteca DAO anteriores à versão 3.6 não são fornecidas e nem têm suporte no Access.

## <a name="dao-to-ado-object-map"></a>De DAO para mapa de objeto ADO

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><strong>DAO</strong></p></th>
<th><p><strong>ADO (ADODB)</strong></p></th>
<th><p><strong>Observação</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBEngine</p></td>
<td><p>Nenhum</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Espaço de trabalho</p></td>
<td><p>Nenhum</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Banco de dados</p></td>
<td><p>Conexão</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Conjunto de Registros</p></td>
<td><p>Conjunto de Registros</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Dynaset-Type</p></td>
<td><p>Conjunto de chaves</p></td>
<td><p>Recupera um conjunto de ponteiros para os registros no conjunto de registros.</p></td>
</tr>
<tr class="even">
<td><p>Tipo de instantâneo</p></td>
<td><p>Estático</p></td>
<td><p>Recupera registros completos, mas um conjunto de registros Estáticos não pode ser atualizado.</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>Conjunto de chaves com opção adCmdTableDirect.</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Campo</p></td>
<td><p>Campo</p></td>
<td><p>Quando mencionado em um conjunto de registros.</p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a>DAO

#### <a name="open-a-recordset"></a>Abrir um Conjunto de Registros

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a>Editar um Conjunto de Registros

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a>ADO

#### <a name="open-a-recordset"></a>Abrir um Conjunto de Registros

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a>Editar um Conjunto de Registros

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> O deslocamento do foco do registro atual por meio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sem usar primeiro o método **CancelUpdate** executará implicitamente o método **Update**.

### <a name="about-the-contributors"></a>Sobre os colaboradores

**Link fornecido pela** comunidade [UtterAccess](https://www.utteraccess.com). UtterAccess é o fórum principal de wiki e de ajuda do Microsoft Access.

- [Escolher entre DAO e ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

