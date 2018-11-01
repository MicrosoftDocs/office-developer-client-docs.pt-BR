---
title: Propriedade DrilledDown (ADO MD)
TOCTitle: DrilledDown Property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7e53eb2a6d1735e07fa73e38adad8a59522fddf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871497"
---
# <a name="drilleddown-property-ado-md"></a>Propriedade DrilledDown (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Indica se nenhum filho segue imediatamente o membro no eixo.

## <a name="return-values"></a>Valor de retorno

Retorna um valor **Boolean** e é somente leitura. **DrilledDown** retornará **True** se não houver membros filho do membro atual no eixo. **DrilledDown** retornará **False** se houver um ou mais membros filho do membro atual no eixo.

## <a name="remarks"></a>Comentários

Use a propriedade **DrilledDown** para determinar se há pelo menos um filho desse membro no eixo imediatamente após esse membro. Essas informações são úteis na exibição do membro.

Somente objetos [Member](member-object-ado-md.md) pertencentes a um objeto [Position](position-object-ado-md.md) oferecem suporte a essa propriedade. Ocorrerá um erro quando ela for referenciada em objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md).

