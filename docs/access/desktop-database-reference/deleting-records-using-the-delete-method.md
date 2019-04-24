---
title: Exclusão de registros com o método Delete
TOCTitle: Deleting records using the Delete method
ms:assetid: 22917c33-4d14-ebab-d85c-2cbe7f68c560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249003(v=office.15)
ms:contentKeyID: 48543708
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a476e9bc57224b0e46afb31bf092450c26de0a17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293963"
---
# <a name="deleting-records-using-the-delete-method"></a>Exclusão de registros com o método Delete


**Aplica-se ao:** Access 2013, Office 2013

O uso do método **Delete** marca o registro atual ou um grupo de registros em um objeto **Recordset**, para exclusão. Se o objeto **Recordset** não permitir a exclusão de registros, ocorrerá um erro. Se você estiver no modo de atualização imediata, as exclusões ocorrerão imediatamente no banco de dados. Se um registro não puder ser excluído com êxito (devido a violações de integridade do banco de dados, por exemplo), ele permanecerá no modo de edição após a chamada para **Update**. Isso significa que você deve cancelar a atualização usando [CancelUpdate](cancelupdate-method-ado.md) antes de mover o registro atual (por exemplo, usando [Close](close-method-ado.md), [Move](move-method-ado.md) ou [NextRecordset](nextrecordset-method-ado.md)).

Se você estiver no modo de atualização em lotes, os registros serão marcados para exclusão a partir do cache e a exclusão propriamente dita ocorrerá quando você chamar o método **UpdateBatch**. (Para exibir os registros excluídos, defina a propriedade **Filter** como **adFilterAffectedRecords** após a chamada de **Delete**.)

A tentativa de recuperar valores de campo do registro excluído gera um erro. Após a exclusão do registro atual, ele permanecerá atual até você passar para um registro diferente. Quando você se move para longe do registro excluído, ele deixa de ser acessível.

Se você aninhar exclusões em uma transação, poderá recuperar registros excluídos usando o método **RollbackTrans**. Se estiver no modo de atualização em lotes, você poderá cancelar uma exclusão ou um grupo de exclusões pendentes usando o método **CancelBatch**.

Se a tentativa de excluir registros falhar devido a um conflito com os dados subjacentes (por exemplo, um registro já foi excluído por outro usuário), o provedor retornará avisos para a coleção **Errors**, mas não interromperá a execução do programa. Um erro em tempo de execução só ocorrerá se houver conflitos em todos os registros solicitados.

Se a propriedade dinâmica **Unique Table** estiver definida e o **Recordset** for o resultado da execução de uma operação JOIN em várias tabelas, o método **Delete** excluirá linhas apenas da tabela nomeada na propriedade **Unique Table**.

O método **Delete** usa um argumento opcional que permite especificar quais registros são afetados pela operação **Delete**. Os únicos valores válidos para esse argumento são uma das seguintes constantes enumeradas **AffectEnum** do ADO:

  - **adAffectCurrent** Afeta somente o registro atual.

  - **adAffectGroup** Afeta somente os registros que satisfazem a configuração atual da propriedade **Filter** . A propriedade **Filter** deve ser definida como um valor **FilterGroupEnum** ou uma matriz de **Bookmarks** para usar essa opção.

O código a seguir mostra um exemplo da especificação de **adAffectGroup** durante a chamada do método **Delete**. Este exemplo adiciona alguns registros ao **Recordset** de exemplo e atualiza o banco de dados. Em seguida, ele filtra o **Recordset** usando a constante enumerada de filtro **adFilterAffectedRecords**, a qual deixa apenas os registro recém-adicionados visíveis no **Recordset**. Finalmente, ele chama o método **Delete** e especifica que todos os registros que satisfazem a configuração atual da propriedade **Filter** (os novos registros) devem ser excluídos.

```vb 
 
'BeginDeleteGroup 
 'add some bogus records 
 With objRs1 
 For i = 0 To 8 
 .AddNew 
 .Fields("CompanyName") = "Shipper Number " & i + 1 
 .Fields("Phone") = "(425) 555-000" & (i + 1) 
 .Update 
 Next i 
 
 're-connect & update 
 .ActiveConnection = GetNewConnection 
 .UpdateBatch 
 
 'filter on newly added records 
 .Filter = adFilterAffectedRecords 
 Debug.Print "Deleting the " & .RecordCount & _ 
 " records you just added." 
 
 'delete the newly added bogus records 
 .Delete adAffectGroup 
 .Filter = adFilterNone 
 Debug.Print .RecordCount & " records remain." 
 
 .Close 
 End With 
'EndDeleteGroup 
```

