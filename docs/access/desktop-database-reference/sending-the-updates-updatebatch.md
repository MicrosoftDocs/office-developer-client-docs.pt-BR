---
title: 'Enviando atualizações: UpdateBatch'
TOCTitle: 'Sending the Updates: UpdateBatch'
ms:assetid: a840b9a7-7ccd-9c31-7951-8921dadf381e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249778(v=office.15)
ms:contentKeyID: 48546898
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df52f5bf2dbada1176a76cda3b77dcbc9966b313
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462705"
---
# <a name="sending-the-updates-updatebatch"></a>Enviando atualizações: UpdateBatch


**Aplica-se a**: Access 2013 | Office 2013

## <a name="sending-the-updates-updatebatch-method"></a>Enviando as atualizações: método UpdateBatch

O código a seguir abre um **Conjunto de registros** em modo de lote definindo a propriedade **LockType** como **adLockBatchOptimistic** e a **CursorLocation** como **adUseClient**. Ele adiciona dois novos registros e altera o valor de um campo em um registro existente, salvando os valores originais, e, em seguida, chama o **UpdateBatch** para enviar as alterações de volta para a fonte de dados.

```vb 
 
'BeginBatchUpdate 
    strSQL = "SELECT ShipperId, CompanyName, Phone FROM Shippers" 
                  
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
     
    ' Change value of Phone field for first record in Recordset, saving value 
    ' for later restoration. 
    intId = objRs1("ShipperId") 
    strPhone = objRs1("Phone") 
     
    objRs1("Phone") = "(111) 555-1111" 
     
    'Add two new records 
    For i = 0 To 1 
        objRs1.AddNew 
        objRs1(1) = "New Shipper #" & CStr((i + 1)) 
        objRs1(2) = "(nnn) 555-" & i & i & i & i 
    Next i 
     
    ' Send the updates 
    objRs1.UpdateBatch 
'EndBatchUpdate 
```

Se você estiver editando o registro atual ou adicionando um novo registro quando chamar o método **UpdateBatch**, o ADO automaticamente chamará o método **Update** para salvar qualquer alteração pendente no registro atual antes de transmitir as alterações em lote para o provedor.
