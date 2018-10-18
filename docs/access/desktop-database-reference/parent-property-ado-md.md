---
title: Propriedade Parent (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10c183c997a3c0b49c74e08f7ef29fbe8c274516
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603333"
---
# <a name="parent-property-ado-md"></a>Propriedade Parent (ADO MD)


**Aplica-se a**: Access 2013 | Office 2013

Indica o membro que é o pai do membro atual em uma hierarquia.

<<<<<<< Cabeça
## <a name="return-values"></a>Valores de retorno
=======
## <a name="return-values"></a>Valor de retorno
>>>>>>> mestre

Retorna um objeto [Member](member-object-ado-md.md) e é somente leitura.

## <a name="remarks"></a>Comentários

Um membro que está no nível superior de uma hierarquia (a raiz) não tem pai. Somente objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a esta propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).

