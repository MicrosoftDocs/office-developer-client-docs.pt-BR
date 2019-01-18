---
title: Propriedade Recordset.UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 14ab955d-1c5a-dc76-8dbf-dbca49816bc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845468(v=office.15)
ms:contentKeyID: 48543391
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101185
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ced8fc78729924ce271aa0fe38d77d287a131f13
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705936"
---
# <a name="recordsetupdateoptions-property-dao"></a>Propriedade Recordset.UpdateOptions (DAO)


**Aplica-se a**: Access 2013, o Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . UpdateOptions

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Quando um modo de lote **[Update](recordset-update-method-dao.md)** for executado, o DAO e a biblioteca de cursores em lotes do cliente criarão uma série de instruções SQL UPDATE para fazer as alterações necessárias. Uma cláusula SQL WHERE será criada para cada atualização com a finalidade de isolar os registros marcados como alterados pela propriedade **[RecordStatus](recordset-recordstatus-property-dao.md)**. Como alguns servidores remotos usam gatilhos ou outras formas para forçar a integridade referencial, é importante limitar, com frequência, os campos que estão sendo atualizados para apenas aqueles afetados pela alteração. 

Para fazer isso, defina a propriedade **UpdateOptions** como uma das constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** ou **dbCriteriaTimeStamp**. Dessa forma, será executada somente a quantidade mínima absoluta de um código do gatilho. Como resultado, a operação de atualização será executada de forma mais rápida e com menos erros potenciais.

Você também pode concatenar qualquer uma das constantes **dbCriteriaDeleteInsert** ou **dbCriteriaUpdate** para determinar se será necessário usar um conjunto de instruções SQL DELETE e INSERT ou uma instrução SQL UPDATE para cada atualização durante o envio das modificações em lotes de volta para o servidor. No caso anterior, foram necessárias duas operações separadas para atualizar o registro. Em alguns casos, especialmente naqueles em que o sistema remoto implementou os gatilhos DELETE, INSERT e UPDATE, a escolha da definição da propriedade **UpdateOptions** correta pode impactar, de forma significativa, o desempenho.

Se você não especificar nenhuma constante, serão usadas **dbCriteriaUpdate** e **dbCriteriaKey**.

Os registros recentemente adicionados sempre gerarão instruções INSERT e os registros excluídos sempre gerarão instruções DELETE, de modo que essa propriedade se aplicará somente na forma como a bibiloteca de cursores atualizará os registros modificados.

## <a name="example"></a>Exemplo

Este exemplo usa as propriedades **BatchSize** e **UpdateOptions** para controlar os aspectos de qualquer atualização em lotes de um objeto **Recordset** específico.

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

