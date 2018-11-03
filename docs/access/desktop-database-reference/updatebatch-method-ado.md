---
title: Método UpdateBatch (ADO)
TOCTitle: UpdateBatch method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ce946d3354f6bbf05ac3819efc5f96c436fa174
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950122"
---
# <a name="updatebatch-method-ado"></a>Método UpdateBatch (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Grava todas as atualizações em lote pendentes no disco.

## <a name="syntax"></a>Sintaxe

*conjunto de registros*. UpdateBatch*AffectRecords*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*AffectRecords* |Opcional. Um valor [AffectEnum](affectenum.md) que indica quantos registros o método **UpdateBatch** afetará.|

## <a name="remarks"></a>Comentários

Utilize o método **UpdateBatch** ao modificar um objeto **Recordset** no modo de atualização em lote a fim de transmitir todas as alterações feitas em um objeto **Recordset** para o banco de dados base.

Se o objeto **Recordset** suportar atualização em lote, você poderá armazenar localmente em cache diversas alterações em um ou mais registros até chamar o método **UpdateBatch**. Se estiver editando o registro atual ou adicionando um novo registro ao chamar o método **UpdateBatch**, o ADO chamará automaticamente o método [Update](update-method-ado.md) para salvar quaisquer informações pendentes no registro atual antes de transmitir as alterações em lote ao provedor. Você deve utilizar a atualização em lote apenas com um conjunto de chaves ou um cursor estático.

> [!NOTE]
> [!OBSERVAçãO] A especificação de **adAffectGroup** como o valor para esse parâmetro resultará em um erro quando não existirem registros visíveis no **Recordset** atual (tal como um filtro ao qual nenhum registro corresponde).

Se a tentativa de transmitir alterações falhar para algum ou todos os registros devido a um conflito com os dados base (por exemplo, um registro já foi excluído por outro usuário), o provedor retornará avisos para a coleção [Errors](errors-collection-ado.md) e ocorrerá um erro em tempo de execução. Utilize a propriedade [Filter](filter-property-ado.md) (**adFilterAffectedRecords**) e a propriedade [Status](status-property-ado-recordset.md) para localizar registros com conflitos.

Para cancelar todas as atualizações em lote pendentes, utilize o método [CancelBatch](cancelbatch-method-ado.md).

Se as propriedades dinâmicas [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) e [Update Resync](update-resync-property-dynamic-ado.md)forem definidas e o **Recordset** for o resultado da execução de uma operação JOIN em várias tabelas, então a execução do método **UpdateBatch** será implicitamente seguida pelo método [Resync](resync-method-ado.md), dependendo das definições da propriedade **Update Resync**.

A ordem na qual as atualizações individuais de um lote são executadas na fonte de dados não é necessariamente a mesma que a ordem na qual elas foram executadas no **Recordset** local. A ordem da atualização depende do provedor. Leve isso em consideração ao codificar atualizações que estão relacionadas entre si, tais como restrições de chave estrangeira ou uma inserção ou atualização.

