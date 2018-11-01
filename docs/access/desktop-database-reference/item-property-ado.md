---
title: Propriedade Item (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73e6240b92a34a6ff1d215cd3211a844f10fe766
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868305"
---
# <a name="item-property-ado"></a>Propriedade Item (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Indica um membro específico de uma coleção, por nome ou número ordinal.

## <a name="syntax"></a>Sintaxe

Definir o*objeto* = *conjunto*. Item (Index)

## <a name="return-value"></a>Valor de retorno

Retorna uma referência de objeto.

## <a name="parameters"></a>Parâmetros

- *Index*

- Uma expressão **Variant** avaliada para o nome ou para o número ordinal de um objeto em uma coleção.

## <a name="remarks"></a>Comentários

Use a propriedade **Item** para retornar um objeto específico em uma coleção. Se o **Item** não puder encontrar um objeto da coleção correspondente ao argumento de *índice* , ocorrerá um erro. Além disso, algumas coleções não oferecem suporte a objetos nomeados; para essas coleções, use referências de números ordinais.

A propriedade **Item** é a propriedade padrão para todas as coleções; assim, os formulários de sintaxe a seguir são intercambiáveis:

```vb
    collection.Item (Index)
    collection (Index)
```
