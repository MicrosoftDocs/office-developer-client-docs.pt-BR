---
title: Método Requery (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0105fb67c095355e607c6c73fc73fc4c6b1050ed
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998180"
---
# <a name="requery-method-ado"></a>Método Requery (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Atualiza os dados em um objeto [Recordset](recordset-object-ado.md), reexecutando a consulta que serve de base ao objeto.

## <a name="syntax"></a>Sintaxe

*conjunto de registros*. *Opções* de Requery

## <a name="parameters"></a>Parâmetros

|Nome |Descrição|
|:----|:----------|
|*Options* |Opcional. Um bitmask contendo os valores [ExecuteOptionEnum](executeoptionenum.md) e [CommandTypeEnum](commandtypeenum.md) que afetam esta operação.|

> [!NOTE]
> Se *Options* for definido como **adAsyncExecute**, esta operação será executada de forma assíncrona e um evento [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) será emitido quando ela for concluída.

O valor **adExecuteNoRecords** ou **adExecuteStream** de **ExecuteOpenEnum** não deve ser usado com **Requery**.

## <a name="remarks"></a>Comentários

Use o método **Requery** para atualizar todo o conteúdo de um objeto **Recordset** a partir da fonte de dados, emitindo novamente o comando original e recuperando os dados uma segunda vez. A chamada desse método equivale à chamada dos métodos [Close](close-method-ado.md) e [Open](open-method-ado-recordset.md) sucessivamente. Se você estiver editando o registro atual ou adicionando um novo registro, ocorrerá erro.

Enquanto o objeto **Recordset** estiver aberto, as propriedades que definem a natureza do cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md) etc.) serão somente leitura. Portanto, o método **Requery** somente poderá atualizar o cursor atual. Para alterar qualquer propriedade do cursor e exibir os resultados, use o método [Close](close-method-ado.md) para tornar as propriedades novamente como leitura/gravação. Em seguida, você poderá alterar as configurações de propriedade e chamar o método [Open](open-method-ado-recordset.md) para reabrir o cursor.

