---
title: Método SkipLine (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e49b8379f078ad698a4a0040de0eb2e4429fd34
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718774"
---
# <a name="skipline-method-ado"></a>Método SkipLine (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Ignora uma linha inteira ao ler um fluxo de texto.

## <a name="syntax"></a>Sintaxe

*Stream*. SkipLine

## <a name="remarks"></a>Comentários

Todos os caracteres até e incluindo o próximo separador de próxima, serão ignorados. Por padrão, o [LineSeparator](lineseparator-property-ado.md) é **adCRLF**. Se você tentar ignorar além do [EOS](eos-property-ado.md), a posição atual simplesmente permanecerá no **EOS**.

O método **SkipLine** é utilizado com fluxos de texto ([Type](type-property-ado-stream.md) é **adTypeText**).

