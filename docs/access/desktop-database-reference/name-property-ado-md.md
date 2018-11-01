---
title: Propriedade Name (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63e098a8b97bb37fad2ef256affb2da142daf434
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878644"
---
# <a name="name-property-ado-md"></a>Propriedade Name (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Indica o nome de um objeto

## <a name="return-values"></a>Valor de retorno

Retorna um objeto **String** e é somente leitura.

## <a name="remarks"></a>Comentários

Você pode recuperar a propriedade **Name** de um objeto por uma referência ordinal e, depois, fazer referência ao objeto diretamente pelo nome. Por exemplo, se cdf.CubeDefs(0).Name gerar "Bobs Video Store", você poderá fazer referência a esse [CubeDef](cubedef-object-ado-md.md) como cdf.CubeDefs("Bobs Video Store").

