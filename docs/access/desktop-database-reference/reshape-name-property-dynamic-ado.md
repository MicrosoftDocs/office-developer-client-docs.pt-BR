---
title: Propriedade reshape Name dinâmica (ADO)
TOCTitle: Reshape Name dynamic property (ADO)
ms:assetid: 59ef99c8-da40-5cf6-b987-d47ea1433f45
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249307(v=office.15)
ms:contentKeyID: 48545030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b5d8436979703a00f63c93e5d8cd426d190fecfc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926161"
---
# <a name="reshape-name-dynamic-property-ado"></a>Propriedade reshape Name dinâmica (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Especifica um nome para o objeto [Recordset](recordset-object-ado.md).

## <a name="return-values"></a>Valor de retorno

Retorna um valor **String** que é o nome do **Recordset**.

## <a name="remarks"></a>Comentários

Os nomes persistem enquanto durar a conexão ou até o **Recordset** ser fechado.

A propriedade **Reshape Name** é usada, basicamente, com o recurso de remodelagem do provedor de serviço [Microsoft Data Shaping Service para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md). Para tomar parte na remodelagem, os nomes devem ser exclusivos.

Essa propriedade é somente leitura, mas ela pode ser definida indiretamente quando um Recordset é criado. Por exemplo, se uma cláusula de um comando SHAPE criar um Recordset e der um nome nome de alias sem a palavra-chave "AS" , o alias será atribuído à propriedade Reshape Name. Se nenhum alias for declarado, então será atribuído à propriedade Reshape Name um nome exclusivo gerado pelo serviço de data shaping. Se o nome alias for o mesmo nome de um **Recordset** existente, nenhum dos **Recordset** será remodelado até que um deles seja liberado. O comportamento padrão pode ser alterado definindo-se a propriedade "Unique Reshape Names" (Consulte "Microsoft Data shaping service para OLE DB") na conexão ADO como TRUE. Isso dará ao serviço de data shaping a permissão para alterar os nomes de usuário atribuídos, se necessário, para garantir a exclusividade.

Use a propriedade **Reshape Name** quando quiser se referir a um **Recordset** em um comando SHAPE ou quando não souber o seu nome porque ele foi gerado pelo Data Shaping Service. Neste caso, é possível gerar um comando SHAPE concatenando o comando da sequência retornada pela propriedade **Reshape Name**.

**Reshape Name** é uma propriedade dinâmica acrescentada à coleção **Properties** do objeto [Recordset](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) estiver configurada como **adUseClient**.

