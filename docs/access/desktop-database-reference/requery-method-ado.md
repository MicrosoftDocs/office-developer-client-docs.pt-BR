---
title: Método Requery (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dc236d730cf773ec38fe5dd903cb64ca9b594
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306710"
---
# <a name="requery-method-ado"></a>Método Requery (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Atualiza os dados em um objeto [Recordset](recordset-object-ado.md), reexecutando a consulta que serve de base ao objeto.

## <a name="syntax"></a>Sintaxe

*recordset*. Opções de *repetir a configuração*

## <a name="parameters"></a>Parâmetros

|Nome |Descrição|
|:----|:----------|
|*Opções* |Opcional. Um bitmask contendo os valores [ExecuteOptionEnum](executeoptionenum.md) e [CommandTypeEnum](commandtypeenum.md) que afetam esta operação.|

> [!NOTE]
> Se *Options* for definido como **adAsyncExecute**, essa operação será executada de forma assíncrona e um evento [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) será emitido quando for concluído.

O valor **adExecuteNoRecords** ou **adExecuteStream** de **ExecuteOpenEnum** não deve ser usado com **Requery**.

## <a name="remarks"></a>Comentários

Use o método **Requery** para atualizar todo o conteúdo de um objeto **Recordset** a partir da fonte de dados, emitindo novamente o comando original e recuperando os dados uma segunda vez. A chamada desse método equivale à chamada dos métodos [Close](close-method-ado.md) e [Open](open-method-ado-recordset.md) sucessivamente. Se você estiver editando o registro atual ou adicionando um novo registro, ocorrerá erro.

Enquanto o objeto **Recordset** estiver aberto, as propriedades que definem a natureza do cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md) etc.) serão somente leitura. Portanto, o método **Requery** somente poderá atualizar o cursor atual. Para alterar qualquer propriedade do cursor e exibir os resultados, use o método [Close](close-method-ado.md) para tornar as propriedades novamente como leitura/gravação. Em seguida, você poderá alterar as configurações de propriedade e chamar o método [Open](open-method-ado-recordset.md) para reabrir o cursor.

