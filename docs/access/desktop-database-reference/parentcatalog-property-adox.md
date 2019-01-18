---
title: Propriedade ParentCatalog (ADOX)
TOCTitle: ParentCatalog property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d7a10bac3c02a771518038351bc4d0b780c0e774
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707455"
---
# <a name="parentcatalog-property-adox"></a>Propriedade ParentCatalog (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

Especifica o catálogo pai de um tabela ou coluna para conceder acesso a propriedades específicas do provedor.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define e retorna um objeto [Catalog](catalog-object-adox.md). A definição de **ParentCatalog** como um objeto **Catalog** aberto permite acessar propriedades específicas do provedor antes de acrescentar uma tabela ou coluna a uma coleção **Catalog**.

## <a name="remarks"></a>Comentários

Alguns provedores de dados permitem que valores de propriedade específicos do provedor sejam gravados somente na fase de criação (quando uma tabela ou coluna é acrescentada à sua coleção **Catalog** ). Para acessar essas propriedades antes de acrescentar esses objetos a um **Catalog**, especifique primeiro o objeto **Catalog** na propriedade **ParentCatalog**.

Ocorre um erro quando a tabela ou coluna é acrescentada a um objeto **Catalog** que não seja **ParentCatalog**.

