---
title: Propriedade DateModified (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: daf72804d51c18b5875e607ce5fdb0dfe20f406c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726075"
---
# <a name="datemodified-property-adox"></a>Propriedade DateModified (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

Indica a data da última modificação do objeto.

## <a name="return-values"></a>Valores de retorno

Retorna um valor **Variant** que especifica a data de modificação. O valor será nulo se o provedor não oferecer suporte a **DateModified**.

## <a name="remarks"></a>Comentários

A propriedade **DateModified** será nula para objetos recém-acrescentados. Após acrescentar um novo [Modo de exibição](view-object-adox.md) ou [Procedimento](procedure-object-adox.md), chame o método [Refresh](refresh-method-ado.md) da coleção [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) para obter valores da propriedade **DateModified**.

