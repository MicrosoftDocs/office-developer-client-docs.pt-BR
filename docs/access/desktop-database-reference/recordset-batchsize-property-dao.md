---
title: Propriedade Recordset.BatchSize (DAO)
TOCTitle: BatchSize Property
ms:assetid: f03dc505-682f-4b60-62f2-1bd088d873c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836544(v=office.15)
ms:contentKeyID: 48548599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101179
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7693f89f07413772ea961a61c86e9c5448c4c449
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300662"
---
# <a name="recordsetbatchsize-property-dao"></a>Propriedade Recordset.BatchSize (DAO)


**Aplica-se ao:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . BatchSize

*expression* Uma variável que representa um objeto **Recordset**.

## <a name="remarks"></a>Comentários

A propriedade **BatchSize** determina o tamanho do lote usado durante o envio de instruções para o servidor em uma atualização em lotes. O valor da propriedade determina o número de instruções enviadas para o servidor em um buffer de comando. Por padrão, 15 instruções são enviados para o servidor em cada lote. Essa propriedade pode ser alterada a qualquer momento. Se um servidor do banco de dados não oferecer suporte ao lote de instruções, você poderá definir essa propriedade como 1, o que fará com que cada instrução seja enviada separadamente.

## <a name="example"></a>Exemplo

Este exemplo usa as propriedades **BatchSize** e **UpdateOptions** para controlar os aspectos de qualquer atualização em lotes para o objeto Recordset especificado.

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

