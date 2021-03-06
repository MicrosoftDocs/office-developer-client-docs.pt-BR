---
title: Método CancelUpdate (ADO)
TOCTitle: CancelUpdate method (ADO)
ms:assetid: 2bd4d168-ba52-7786-5046-44febeda88e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249065(v=office.15)
ms:contentKeyID: 48543938
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4585679688929532d7f50be9efc71b2830bb6587
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296623"
---
# <a name="cancelupdate-method-ado"></a>Método CancelUpdate (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Cancela qualquer alteração feita na linha atual ou na nova linha de um objeto [Recordset](recordset-object-ado.md), ou na coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md), antes da chamada do método [Update](update-method-ado.md).

## <a name="syntax"></a>Sintaxe

*recordset*. CancelUpdate

*registro*. *Campos*. CancelUpdate

## <a name="remarks"></a>Comentários

**Objeto Recordset**

Use o método **CancelUpdate** para cancelar as alterações feitas na linha atual ou descartar uma linha recém-adicionada. Você não poderá cancelar as alterações feitas na linha atual ou em uma nova linha após chamar o método **Update**, a menos que as alterações façam parte de uma transação que possa ser revertida com o método [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) ou façam parte de uma atualização em lotes. No caso de uma atualização em lotes, você poderá cancelar **Update** com o método **CancelUpdate** ou [CancelBatch](cancelbatch-method-ado.md).

Se, ao chamar o método **CancelUpdate**, você estiver adicionando uma nova linha, a linha atual passará a ser a linha que estava atual antes da chamada de [AddNew](addnew-method-ado.md).

Se estiver no modo de edição e desejar sair do registro atual (por exemplo, com [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) ou [Close](close-method-ado.md)), você poderá usar **CancelUpdate** para cancelar as alterações pendentes. Esse procedimento será necessário se a atualização não puder ser postada com êxito na fontes de dados (por exemplo, a falha de uma tentativa de exclusão devido a violações de integridade referencial manterá o **Recordset** no modo de edição depois que [Delete](delete-method-ado-recordset.md) for chamado).

**Objeto Record**

O método **CancelUpdate** cancela qualquer inserção ou exclusão pendente de objetos [Field](field-object-ado.md), e também cancela as atualizações pendentes de campos existentes, restaurando-os aos seus valores originais. A propriedade [Status](status-property-ado-recordset.md) de todos os campos na coleção **Fields** é definida como **adFieldOK**.

