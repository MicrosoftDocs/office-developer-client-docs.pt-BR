---
title: Propriedade Item (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4afbb31fb95aeea66d9cf93624b95c8796e2d25
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949359"
---
# <a name="item-property-ado"></a>Propriedade Item (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Indica um membro específico de uma coleção, por nome ou número ordinal.

## <a name="syntax"></a>Sintaxe

Definir o*objeto* = *conjunto*. Item (Index)

## <a name="return-value"></a>Valor de retorno

Retorna uma referência de objeto.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Index* |Uma expressão **Variant** avaliada para o nome ou para o número ordinal de um objeto em uma coleção.|

## <a name="remarks"></a>Comentários

Use a propriedade **Item** para retornar um objeto específico em uma coleção. Se o **Item** não puder encontrar um objeto da coleção correspondente ao argumento de *índice* , ocorrerá um erro. Além disso, algumas coleções não oferecem suporte a objetos nomeados; para essas coleções, use referências de números ordinais.

A propriedade **Item** é a propriedade padrão para todas as coleções; assim, os formulários de sintaxe a seguir são intercambiáveis:

```vb
    collection.Item (Index)
    collection (Index)
```
