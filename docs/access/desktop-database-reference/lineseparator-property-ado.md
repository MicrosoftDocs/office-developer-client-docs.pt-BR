---
title: Propriedade LineSeparator (ADO)
TOCTitle: LineSeparator Property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1aee67410e2abf921bdbd61e6cd8573e090fafd9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463966"
---
# <a name="lineseparator-property-ado"></a>Propriedade LineSeparator (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica o caractere binário a ser usado como o separador de linha nos objetos [Stream](stream-object-ado.md) de texto.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [LineSeparatorsEnum](lineseparatorsenum.md) que indica o caractere do separador de linha usado no **Stream**. O valor padrão é **adCRLF**.

## <a name="remarks"></a>Comentários

**LineSeparator** é usada para interpretar as linhas ao ler o conteúdo de um **Stream** de texto. As linhas podem ser ignoradas com o método [SkipLine](skipline-method-ado.md).

**LineSeparator** é usada apenas com objetos **Stream** de texto ([Type](type-property-ado-stream.md) é **adTypeText**). Esta propriedade será ignorada se **Type** for **adTypeBinary**.

