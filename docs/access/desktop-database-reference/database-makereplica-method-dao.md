---
title: Método Database.MakeReplica (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 632bf0af35dd49951d58ba126b6e03678a1a12db
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950248"
---
# <a name="databasemakereplica-method-dao"></a>Método Database.MakeReplica (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Cria uma nova réplica a partir de uma outra réplica do banco de dados (somente espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . MakeReplica (***PathName***, ***Descrição***, ***Opções***)

*expressão* Uma variável que representa um objeto de **banco de dados** .

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Nome do caminho</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Cadeia de caracteres</strong></p></td>
<td><p>O caminho e o nome de arquivo da nova réplica. Se réplica for um nome de arquivo existente, ocorrerá um erro.</p></td>
</tr>
<tr class="even">
<td><p><em>Descrição</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Cadeia de caracteres</strong></p></td>
<td><p>A <strong>String</strong> que descreve a réplica que está sendo criada</p></td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma constante <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> que especifica as características da réplica que você está criando.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Uma réplica parcial recém-criada terá todas as propriedades **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** definidas como **False**, o que significa que nenhum dado estará nas tabelas.

## <a name="example"></a>Exemplo

Esta função usa o método **MakeReplica** para criar uma réplica adicional de um Design Mestre existente. O argumento intOptions pode ser uma combinação das constantes **dbRepMakeReadOnly** e **dbRepMakePartial**ou pode ser 0. Por exemplo, para criar uma réplica parcial somente leitura, você deve passar o valor **dbRepMakeReadOnly** + **dbRepMakePartial** como o valor do intOptions.

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```

