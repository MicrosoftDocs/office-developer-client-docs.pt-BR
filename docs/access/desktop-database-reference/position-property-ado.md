---
title: Propriedade Position (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab1111cdbc0e5a319f1f3431477854c6d38eff20
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875403"
---
# <a name="position-property-ado"></a>Propriedade Position (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica a posição atual em um objeto [Stream](stream-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que especifica o deslocamento, em número de bytes, da posição atual a partir do início do fluxo. O padrão é 0, que representa o primeiro byte no fluxo.

## <a name="remarks"></a>Comentários

A posição atual pode ser movida para um ponto posterior ao final do fluxo. Se você especificar a posição atual além do final do fluxo, o [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) do objeto **Stream** aumentará de forma adequada. Os bytes novos adicionados desta forma serão nulos.


> [!NOTE]
> <P>[!OBSERVAçãO] <STRONG>Position</STRONG> sempre mede bytes. Para fluxos de texto que utilizam conjuntos de caracteres com vários bytes, multiplique a posição pelo tamanho do caractere para determinar o número do caractere. Por exemplo, para um conjunto de caracteres de dois bytes, o primeiro caractere estará na posição 0, o segundo caractere na posição 2, o terceiro na posição 4, e assim por diante.</P>



Os valores negativos não podem ser utilizados para alterar a posição atual em um **Stream**. Somente números positivos podem ser utilizados para **Position**.

Para objetos **Stream** somente leitura, o ADO não retornará um erro se **Position** for definida com um valor superior ao **Size** do **Stream**. Isto não altera o tamanho do **Stream** nem do conteúdo do **Stream**. Entretanto, esse procedimento deve ser evitado, pois resulta em um valor **Position** insignificante.

