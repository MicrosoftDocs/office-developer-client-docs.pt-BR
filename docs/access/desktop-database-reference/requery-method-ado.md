---
title: Método Requery (ADO)
TOCTitle: Requery Method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3fde13d923a67ca995cdb3e7f59a327e82a9688
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464000"
---
# <a name="requery-method-ado"></a>Método Requery (ADO)


**Aplica-se a**: Access 2013 | Office 2013



Atualiza os dados em um objeto [Recordset](recordset-object-ado.md), reexecutando a consulta que serve de base ao objeto.

## <a name="syntax"></a>Sintaxe

*conjunto de registros*. *Opções* de Requery

## <a name="parameter"></a>Parâmetro

  - *Options*

  - Opcional. Um bitmask contendo os valores [ExecuteOptionEnum](executeoptionenum.md) e [CommandTypeEnum](commandtypeenum.md) que afetam esta operação.


> [!NOTE]
> <P>Se <EM>Options</EM> for definido como <STRONG>adAsyncExecute</STRONG>, esta operação será executada de forma assíncrona e um evento <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> será emitido quando ela for concluída.</P>



O valor **adExecuteNoRecords** ou **adExecuteStream** de **ExecuteOpenEnum** não deve ser usado com **Requery**.

## <a name="remarks"></a>Comentários

Use o método **Requery** para atualizar todo o conteúdo de um objeto **Recordset** a partir da fonte de dados, emitindo novamente o comando original e recuperando os dados uma segunda vez. A chamada desse método equivale à chamada dos métodos [Close](close-method-ado.md) e [Open](open-method-ado-recordset.md) sucessivamente. Se você estiver editando o registro atual ou adicionando um novo registro, ocorrerá erro.

Enquanto o objeto **Recordset** estiver aberto, as propriedades que definem a natureza do cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md) etc.) serão somente leitura. Portanto, o método **Requery** somente poderá atualizar o cursor atual. Para alterar qualquer propriedade do cursor e exibir os resultados, use o método [Close](close-method-ado.md) para tornar as propriedades novamente como leitura/gravação. Em seguida, você poderá alterar as configurações de propriedade e chamar o método [Open](open-method-ado-recordset.md) para reabrir o cursor.

