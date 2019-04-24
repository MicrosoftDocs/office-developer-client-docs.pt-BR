---
title: Propriedade DateCreated (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 59b19ab3be6633daf7295a63a33a31a34b64fbd7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294418"
---
# <a name="datecreated-property-adox"></a>Propriedade DateCreated (ADOX)


**Aplica-se ao:** Access 2013, Office 2013

Indica a data de criação do objeto.

## <a name="return-values"></a>Valor de retorno

Retorna um valor **Variant** que especifica a data de criação. O valor será nulo se o provedor não oferecer suporte a **DateCreated**.

## <a name="remarks"></a>Comentários

A propriedade **DateCreated** é nula para objetos recém-acrescentados. Após acrescentar um novo [Modo de exibição](view-object-adox.md) ou [Procedimento](procedure-object-adox.md), chame o método [Refresh](refresh-method-ado.md) da coleção [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) para obter valores da propriedade **DateCreated**.

