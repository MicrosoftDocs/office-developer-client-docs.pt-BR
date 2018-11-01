---
title: Método SkipLine (ADO)
TOCTitle: SkipLine Method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c1ab54402dac8f6721c4c12f55f07979c4adff4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885448"
---
# <a name="skipline-method-ado"></a>Método SkipLine (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Ignora uma linha inteira ao ler um fluxo de texto.

## <a name="syntax"></a>Sintaxe

*Stream*. SkipLine

## <a name="remarks"></a>Comentários

Todos os caracteres até e incluindo o próximo separador de próxima, serão ignorados. Por padrão, o [LineSeparator](lineseparator-property-ado.md) é **adCRLF**. Se você tentar ignorar além do [EOS](eos-property-ado.md), a posição atual simplesmente permanecerá no **EOS**.

O método **SkipLine** é utilizado com fluxos de texto ([Type](type-property-ado-stream.md) é **adTypeText**).

