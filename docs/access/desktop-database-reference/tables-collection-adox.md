---
title: Coleção Tables (ADOX)
TOCTitle: Tables collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e53cd4b6d4a61a226103eb443bac7f3b4f92d908
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716165"
---
# <a name="tables-collection-adox"></a>Coleção Tables (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

Contém todos os objetos [Tabela](table-object-adox.md) de um catálogo.

## <a name="remarks"></a>Comentários

O método [Append](append-method-adox-tables.md) de uma coleção **Tables** é exclusivo de ADOX. Você pode:

  - Adicionar uma nova tabela à coleção com o método **Append**.

As propriedades e os métodos restantes são padrão das coleções do ADO. Você pode:

  - Acessar uma tabela na coleção com a propriedade [Item](item-property-ado.md).

  - Retornar o número de tabelas contidas na coleção com a propriedade [Count](count-property-ado.md).

  - Remover uma tabela da coleção com o método [Delete](delete-method-adox-collections.md).

  - Atualizar os objetos da coleção para refletir o atual esquema do banco de dados com o método [Refresh](refresh-method-ado.md).

Alguns provedores podem retornar outros objetos de esquema, como modos de exibição, na coleção Tables. Portanto, algumas coleções ADOX podem conter referências ao mesmo objeto. Se você excluir o objeto de uma coleção, a alteração não será visível em outra coleção que faça referência ao objeto excluído até que o método Refresh seja acionado na coleção. Por exemplo, com o OLE DB Provider for Microsoft Jet, modos de exibição são retornados com a coleção Tables. Se cancelar um modo de exibição, você deverá atualizar a coleção Tables para que ela possa refletir a alteração.

