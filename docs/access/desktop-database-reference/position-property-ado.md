---
title: Propriedade Position (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a47cc394cf0bb1c6f5a3d707c1885d0abef0f0e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704228"
---
# <a name="position-property-ado"></a>Propriedade Position (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Indica a posição atual em um objeto [Stream](stream-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que especifica o deslocamento, em número de bytes, da posição atual a partir do início do fluxo. O padrão é 0, que representa o primeiro byte no fluxo.

## <a name="remarks"></a>Comentários

A posição atual pode ser movida para um ponto posterior ao final do fluxo. Se você especificar a posição atual além do final do fluxo, o [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) do objeto **Stream** aumentará de forma adequada. Os bytes novos adicionados desta forma serão nulos.

> [!NOTE]
> [!OBSERVAçãO] **Position** sempre mede bytes. Para fluxos de texto que utilizam conjuntos de caracteres com vários bytes, multiplique a posição pelo tamanho do caractere para determinar o número do caractere. Por exemplo, para um conjunto de caracteres de dois bytes, o primeiro caractere estará na posição 0, o segundo caractere na posição 2, o terceiro na posição 4, e assim por diante.

Os valores negativos não podem ser utilizados para alterar a posição atual em um **Stream**. Somente números positivos podem ser utilizados para **Position**.

Para objetos **Stream** somente leitura, o ADO não retornará um erro se **Position** for definida com um valor superior ao **Size** do **Stream**. Isto não altera o tamanho do **Stream** nem do conteúdo do **Stream**. Entretanto, esse procedimento deve ser evitado, pois resulta em um valor **Position** insignificante.

