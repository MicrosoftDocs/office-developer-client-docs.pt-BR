---
title: Método Resync (ADO)
TOCTitle: Resync method (ADO)
ms:assetid: f594a200-56e6-fcf5-9b0a-900c56377f24
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250251(v=office.15)
ms:contentKeyID: 48548717
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fa483d86dc345968607a0752f0552ddccfe7fef5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306570"
---
# <a name="resync-method-ado"></a>Método Resync (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Atualiza os dados no objeto [Recordset](recordset-object-ado.md) atual, ou a coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md), a partir do banco de dados subjacente.

## <a name="syntax"></a>Sintaxe

*Recordset*. Ressincronizar*AffectRecords*, *ResyncValues*

*Record*. *Campos*. Ressincronizar*ResyncValues*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*AffectRecords* |Opcional. Um valor [AffectEnum](affectenum.md) que determina a quantidade de registros que serão afetados pelo método **Resync**. O valor padrão é **adAffectAll**. Esse valor não está disponível com o método **Resync** da coleção **Fields** de um objeto **Record**.|
|*ResyncValues* |Opcional. Um valor [ResyncEnum](resyncenum.md) que especifica se os valores subjacentes serão substituídos. O valor padrão é **adResyncAllValues**.|

## <a name="remarks"></a>Comentários

### <a name="recordset"></a>Recordset

Use o método **Resync** para sincronizar novamente os registros do **Recordset** atual com o banco de dados subjacente. Esse procedimento será útil se você estiver usando um cursor estático ou somente de encaminhamento e desejar ver as alterações no banco de dados subjacente.

Se você definir a propriedade [CursorLocation](cursorlocation-property-ado.md) como **adUseClient**, **Resync** somente estará disponível para os objetos **Recordset** que não sejam somente leitura.

Diferente do método [Requery](requery-method-ado.md), o método **Resync** não reexecuta o comando subjacente do objeto **Recordset**. Os novos registros no banco de dados subjacente não estarão visíveis.

Se a tentativa de nova sincronização falhar devido a um conflito com os dados subjacentes (por exemplo, por causa da exclusão de um registro por outro usuário), o provedor retornará avisos à coleção [Errors](errors-collection-ado.md) e ocorrerá um erro em tempo de execução. Use a propriedade [Filter](filter-property-ado.md) (**adFilterConflictingRecords**) e a propriedade [Status](status-property-ado-recordset.md) para localizar registros com conflitos.

Se as propriedades dinâmicas [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) e [Resync Command](resync-command-property-dynamic-ado.md) forem definidas e **Recordset** resultar da execução de uma operação JOIN em várias tabelas, o método **Resync** executará o comando fornecido na propriedade **Resync Command** somente na tabela nomeada na propriedade **Unique Table**.

### <a name="fields"></a>Campos

Use o método **Resync** para sincronizar novamente os valores da coleção **Fields** de um objeto  **Record** com a fonte de dados subjacente. A propriedade [Count](count-property-ado.md) não é afetada por esse método.

Se *ResyncValues* for definido como **adResyncAllValues** (o valor padrão), ocorrerá sincronização das propriedades [UnderlyingValue](underlyingvalue-property-ado.md), [Value](value-property-ado.md) e [OriginalValue](originalvalue-property-ado.md) dos objetos [Field](field-object-ado.md) da coleção. Se *ResyncValues* for definido como **adResyncUnderlyingValues**, somente a propriedade **UnderlyingValue** será sincronizada.

O valor da propriedade **Status** para cada objeto **Field** no momento da chamada também afeta o comportamento de **Resync**. **Resync** não terá efeito para os objetos **Field** com valor **adFieldPendingUnknown** ou **adFieldPendingInsert** para **Status**. Para o valor **adFieldPendingChange** ou **adFieldPendingDelete** de **Status**, **Resync** sincronizará os valores de dados dos campos ainda existentes na fonte de dados.

**Resync** will not modify **Status** values of **Field** objects unless an error occurs when **Resync** is called. For example, if the field no longer exists, the provider will return an appropriate **Status** value for the **Field** object, such as **adFieldDoesNotExist**. Returned **Status** values may be logically combined within the value of the **Status** property.

