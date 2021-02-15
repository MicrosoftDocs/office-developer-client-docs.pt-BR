---
title: Método Delete (Recordset do ADO)
TOCTitle: Delete method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e8142d4fc4fc0036f80693f0bff779d9f3f2a62e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294096"
---
# <a name="delete-method-ado-recordset"></a>Método Delete (Recordset do ADO)

**Aplica-se ao:** Access 2013, Office 2013

Exclui o registro atual ou um grupo de registros.

## <a name="syntax"></a>Sintaxe

*recordset*. Excluir *AffectRecords*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*AffectRecords* |Um valor [AffectEnum](affectenum.md) que determina quantos registros o método **Delete** afetará. O valor padrão é **adAffectCurrent**.|

> [!NOTE]
> [!OBSERVAçãO] **adAffectAll** e **adAffectAllChapters** não são argumentos válidos para **Delete**.

## <a name="remarks"></a>Comentários

A utilização do método **Delete** marca o registro atual ou um grupo de registros em um objeto [Recordset](recordset-object-ado.md) para exclusão. Se o objeto **Recordset** não permitir a exclusão de registros, ocorrerá um erro. Se você estiver no modo de atualização imediata, as exclusões ocorrem imediatamente no banco de dados. Se um registro não puder ser excluído com êxito (devido a violações de integridade do banco de dados, por exemplo), o registro permanecerá no modo de edição após a chamada a **Update**. Isso significa que você deve cancelar a atualização com [CancelUpdate](cancelupdate-method-ado.md) antes de mover para fora do registro atual (por exemplo, com [Close](close-method-ado.md), [Move](move-method-ado.md) ou [NextRecordset](nextrecordset-method-ado.md)).

Se você estiver no modo de atualização em lote, os registros são marcados para exclusão no cache e a exclusão real ocorrerá quando você chamar o método [UpdateBatch](updatebatch-method-ado.md). (Utilize a propriedade [Filter](filter-property-ado.md) para ver os registros excluídos.)

A recuperação de valores de campo do registro excluído gera um erro. Depois de excluir o registro atual, o registro excluído permanecerá atual até que você mova para um registro diferente. Depois de mover para fora do registro excluído, ele não mais será acessível.

Se você aninhar exclusões em uma transação, é possível recuperar registros excluídos com o método [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Se você estiver no modo de atualização em lote, poderá cancelar uma exclusão pendente ou um grupo de exclusões pendentes com o método [CancelBatch](cancelbatch-method-ado.md).

Se a tentativa de excluir registros falhar devido a um conflito com os dados subjacentes (por exemplo, um registro já foi excluído por outro usuário), o provedor retornará avisos para a coleção [Errors](errors-collection-ado.md), mas não interromperá a execução do programa. Um erro em tempo de execução só ocorrerá se houver conflitos em todos os registros solicitados.

Se a propriedade dinâmica [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) estiver definida e o **Recordset** for o resultado da execução de uma operação JOIN em várias tabelas, o método **Delete** excluirá linhas apenas da tabela nomeada na propriedade [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).

