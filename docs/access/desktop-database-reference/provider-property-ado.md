---
title: Propriedade Provider (ADO)
TOCTitle: Provider Property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 890f80534ff47c4dea67b34f345bce0f90328c60
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461940"
---
# <a name="provider-property-ado"></a>Propriedade Provider (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica o nome do provedor de um objeto [Connection](connection-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String** que indica o nome do provedor.

## <a name="remarks"></a>Comentários

Utilize a propriedade **Provider** para definir ou retornar o nome do provedor para uma conexão. Essa propriedade também pode ser definida pelo conteúdo da propriedade [ConnectionString](connectionstring-property-ado.md) ou pelo argumento *ConnectionString *  do método [Open](open-method-ado-connection.md); entretanto, a especificação de um provedor em mais de um local enquanto o método **Open** é chamado pode gerar resultados imprevisíveis. Se nenhum provedor for especificado, a propriedade assumirá o padrão de MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).

A propriedade **Provider** é leitura/gravação quando a conexão estiver fechada e somente leitura quando estiver aberta. A definição será efetivada somente após a abertura do objeto **Connection** ou o acesso à coleção [Properties](properties-collection-ado.md) do objeto **Connection**. Haverá erro se a definição não for válida.

