---
title: Propriedade Reshape Name --Dinâmica (ADO)
TOCTitle: Reshape Name Property--Dynamic (ADO)
ms:assetid: 59ef99c8-da40-5cf6-b987-d47ea1433f45
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249307(v=office.15)
ms:contentKeyID: 48545030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f202af564d9e8d3634b895ecf851ddd37e49c4b8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463203"
---
# <a name="reshape-name-property--dynamic-ado"></a>Propriedade Reshape Name --Dinâmica (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Especifica um nome para o objeto [Recordset](recordset-object-ado.md).

## <a name="return-values"></a>Valores de retorno

Retorna um valor **String** que é o nome do **Recordset**.

## <a name="remarks"></a>Comentários

Os nomes persistem enquanto durar a conexão ou até o **Recordset** ser fechado.

A propriedade **Reshape Name** é usada, basicamente, com o recurso de remodelagem do provedor de serviço [Microsoft Data Shaping Service para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md). Para tomar parte na remodelagem, os nomes devem ser exclusivos.

Essa propriedade é somente leitura, mas ela pode ser definida indiretamente quando um Recordset é criado. Por exemplo, se uma cláusula de um comando SHAPE criar um Recordset e der um nome nome de alias sem a palavra-chave "AS" , o alias será atribuído à propriedade Reshape Name. Se nenhum alias for declarado, então será atribuído à propriedade Reshape Name um nome exclusivo gerado pelo serviço de data shaping. Se o nome alias for o mesmo nome de um **Recordset** existente, nenhum dos **Recordset** será remodelado até que um deles seja liberado. O comportamento padrão pode ser alterado definindo-se a propriedade "Unique Reshape Names" (Consulte "Microsoft Data shaping service para OLE DB") na conexão ADO como TRUE. Isso dará ao serviço de data shaping a permissão para alterar os nomes de usuário atribuídos, se necessário, para garantir a exclusividade.

Use a propriedade **Reshape Name** quando quiser se referir a um **Recordset** em um comando SHAPE ou quando não souber o seu nome porque ele foi gerado pelo Data Shaping Service. Neste caso, é possível gerar um comando SHAPE concatenando o comando da sequência retornada pela propriedade **Reshape Name**.

**Reshape Name** é uma propriedade dinâmica acrescentada à coleção **Properties** do objeto [Recordset](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) estiver configurada como **adUseClient**.

