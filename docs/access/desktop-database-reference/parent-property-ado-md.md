---
title: Propriedade Parent (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7beba341a2374e1868c67c8f7b4fab73c71c0ba8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880296"
---
# <a name="parent-property-ado-md"></a>Propriedade Parent (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Indica o membro que é o pai do membro atual em uma hierarquia.

## <a name="return-values"></a>Valor de retorno

Retorna um objeto [Member](member-object-ado-md.md) e é somente leitura.

## <a name="remarks"></a>Comentários

Um membro que está no nível superior de uma hierarquia (a raiz) não tem pai. Somente objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a esta propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).

