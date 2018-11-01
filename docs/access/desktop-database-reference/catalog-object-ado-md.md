---
title: Objeto Catalog (ADO MD)
TOCTitle: Catalog Object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be9d55969a0f90595f25deac0b01a70bff6fc7c3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879596"
---
# <a name="catalog-object-ado-md"></a>Objeto Catalog (ADO MD)


**Aplica-se a**: Access 2013, o Office 2013

Contém informações de esquema multidimensionais (isto é, cubos e dimensões subjacentes, hierarquias, níveis e membros) específicos de um MDP (provedor de dados multidimensionais).

## <a name="remarks"></a>Comentários

Com as coleções e as propriedades de um objeto **Catalog**, você pode fazer o que segue:

  - Abrir o catálogo definindo a propriedade [ActiveConnection](activeconnection-property-ado-md.md) para um objeto [Connection](connection-object-ado.md) do ADO padrão ou para uma sequência de conexão válida.

  - Identificar o **Catálogo** com a propriedade [Name](name-property-ado-md.md).

  - Percorrer os cubos de um catálogo usando a coleção [CubeDefs](cubedefs-collection-ado-md.md).

