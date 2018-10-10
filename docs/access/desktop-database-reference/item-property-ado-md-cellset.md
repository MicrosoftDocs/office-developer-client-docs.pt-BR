---
title: Propriedade Item (ADO MD Cellset)
TOCTitle: Item Property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 017b25b164233cb0e16753874e5b898409b5ac5a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462707"
---
# <a name="item-property-ado-md-cellset"></a>Propriedade Item (ADO MD Cellset)

**Aplica-se a**: Access 2013 | Office 2013

Recupera uma célula de um conjunto de células usando suas coordenadas.

## <a name="syntax"></a>Sintaxe

Definir*célula* = *Cellset*. Item (*posições*)

## <a name="parameters"></a>Parâmetros

- *Positions*

- Um **Variant** **Array** de valores que especificam unicamente uma célula. *Posições* pode ser um destes procedimentos:
    
  - Uma matriz de números de posição
    
  - Uma matriz de nomes de membros
    
  - A posição ordinal

## <a name="remarks"></a>Comentários

Use a propriedade **Item** para retornar um objeto [Cell](cell-object-ado-md.md) em um objeto [Cellset](cellset-object-ado-md.md). Se a propriedade **Item** não puder encontrar a célula correspondente ao argumento *posições* , ocorrerá um erro.

A propriedade **Item** a propriedade padrão do objeto **Cellset**. As seguintes formas sintáticas são intercambiáveis:

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

O argumento *posições* Especifica qual célula para retornar. Você pode especificar a célula por posição ordinal ou por posição ao longo de cada eixo. Ao especificar a célula por posição ao longo de cada eixo, você pode especificar o valor numérico da posição ou dos nomes dos membros de cada posição.

A posição ordinal é um número que identifica uma célula de maneira exclusiva em um **Cellset**. Conceitualmente, células são numeradas em um **Cellset** como se o **Cellset** fosse uma matriz de *p* dimensões, em que *p* é o número de eixos. Células são endereçadas por ordem de linha.

Se nomes de membros são passados como cadeias de caracteres para **Item**, os membros devem ser listados em ordem crescente dos identificadores do eixo numérico. Em um eixo, os membros devem ser listados em ordem crescente de aninhamento de dimensão  ou seja, o membro da dimensão mais externa vem primeiro, seguido dos membros das dimensões internas. Cada dimensão deve ser representada por uma cadeia de caracteres separada, e a lista de cadeias de caracteres de membros deve ser separada por vírgulas.


> [!NOTE]
> [!OBSERVAçãO] Seu provedor de dados pode não oferecer suporte para recuperação de células por nome de membro. Consulte a documentação do seu provedor para obter mais informações.


