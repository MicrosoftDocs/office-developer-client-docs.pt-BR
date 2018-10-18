---
title: Propriedade ParentCatalog (ADOX)
TOCTitle: ParentCatalog Property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9fdd4b41578b4f185d199a47204faabd0af3ff8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603410"
---
# <a name="parentcatalog-property-adox"></a>Propriedade ParentCatalog (ADOX)


**Aplica-se a**: Access 2013 | Office 2013

Especifica o catálogo pai de um tabela ou coluna para conceder acesso a propriedades específicas do provedor.

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define e retorna um objeto [Catalog](catalog-object-adox.md). A definição de **ParentCatalog** como um objeto **Catalog** aberto permite acessar propriedades específicas do provedor antes de acrescentar uma tabela ou coluna a uma coleção **Catalog**.

## <a name="remarks"></a>Comentários

Alguns provedores de dados permitem que valores de propriedade específicos do provedor sejam gravados somente na fase de criação (quando uma tabela ou coluna é acrescentada à sua coleção **Catalog** ). Para acessar essas propriedades antes de acrescentar esses objetos a um **Catalog**, especifique primeiro o objeto **Catalog** na propriedade **ParentCatalog**.

Ocorre um erro quando a tabela ou coluna é acrescentada a um objeto **Catalog** que não seja **ParentCatalog**.

