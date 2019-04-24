---
title: Propriedade Item (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cc38101cb17c52bf2c8c08c08c14163c3772b2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290790"
---
# <a name="item-property-ado"></a>Propriedade Item (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Indica um membro específico de uma coleção, por nome ou número ordinal.

## <a name="syntax"></a>Sintaxe

Definir** = *coleção*de objetos. Item (index)

## <a name="return-value"></a>Valor de retorno

Retorna uma referência de objeto.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Índice* |Uma expressão **Variant** avaliada para o nome ou para o número ordinal de um objeto em uma coleção.|

## <a name="remarks"></a>Comentários

Use a propriedade **Item** para retornar um objeto específico em uma coleção. Um erro ocorrerá se **Item** não puder encontrar um objeto na coleção correspondente ao argumento *Index*. Além disso, algumas coleções não oferecem suporte a objetos nomeados; para essas coleções, use referências de números ordinais.

A propriedade **Item** é a propriedade padrão para todas as coleções; por esse motivo, os seguintes formulários de sintaxe são intercambiáveis:

```vb
    collection.Item (Index)
    collection (Index)
```
