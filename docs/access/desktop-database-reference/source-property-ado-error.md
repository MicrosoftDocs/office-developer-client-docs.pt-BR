---
title: Propriedade Source (Erro do ADO)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd8a2df4462d9f877d1b4451744fc51215227153
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875102"
---
# <a name="source-property-ado-error"></a>Propriedade Source (Erro do ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica o nome do objeto ou aplicativo que gerou originalmente um erro.

## <a name="return-value"></a>Valor de retorno

Retorna um valor **String** que indica o nome de um objeto ou aplicativo.

## <a name="remarks"></a>Comentários

Use a propriedade **Source** em um objeto [Error](error-object-ado.md) para determinar o nome do objeto ou aplicativo que gerou originalmente um erro. Pode ser o nome da classe do objeto ou um identificador programático. Se há erros no ADO, o valor da propriedade será **ADODB. * * * ObjectName*, onde *ObjectName* é o nome do objeto que disparou o erro. Para obter ADO MD e ADOX, o valor será **ADOX. * * * ObjectName* e **ADOMD. * * * ObjectName,* respectivamente.

Com base na documentação de erros das propriedades **Source**, [Number](number-property-ado.md) e [Description](description-property-ado.md) de objetos **Error**, você pode escrever um código que trate o erro apropriadamente.

A propriedade **Source** é somente leitura para objetos **Error**.

