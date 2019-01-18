---
title: Propriedade Name (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4e27870a0c1dbb38b7c0be31c439a95f6aae671
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704151"
---
# <a name="name-property-ado-md"></a>Propriedade Name (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Indica o nome de um objeto

## <a name="return-values"></a>Valores de retorno

Retorna um objeto **String** e é somente leitura.

## <a name="remarks"></a>Comentários

Você pode recuperar a propriedade **Name** de um objeto por uma referência ordinal e, depois, fazer referência ao objeto diretamente pelo nome. Por exemplo, se cdf.CubeDefs(0).Name gerar "Bobs Video Store", você poderá fazer referência a esse [CubeDef](cubedef-object-ado-md.md) como cdf.CubeDefs("Bobs Video Store").

