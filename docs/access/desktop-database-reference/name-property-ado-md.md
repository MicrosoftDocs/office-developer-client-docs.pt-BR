---
title: Propriedade Name (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0cc7a89e0d6b9cdaed2c54d3269b61280ce3306c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462755"
---
# <a name="name-property-ado-md"></a>Propriedade Name (ADO MD)


**Aplica-se a**: Access 2013 | Office 2013

Indica o nome de um objeto.

## <a name="return-values"></a>Valores de retorno

Retorna um objeto **String** e é somente leitura.

## <a name="remarks"></a>Comentários

Você pode recuperar a propriedade **Name** de um objeto por uma referência ordinal e, depois, fazer referência ao objeto diretamente pelo nome. Por exemplo, se cdf.CubeDefs(0).Name gerar "Bobs Video Store", você poderá fazer referência a esse [CubeDef](cubedef-object-ado-md.md) como cdf.CubeDefs("Bobs Video Store").

