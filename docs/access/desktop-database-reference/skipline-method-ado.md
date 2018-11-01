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
# <a name="skipline-method-ado"></a><span data-ttu-id="b5ca9-102">Método SkipLine (ADO)</span><span class="sxs-lookup"><span data-stu-id="b5ca9-102">SkipLine Method (ADO)</span></span>


<span data-ttu-id="b5ca9-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5ca9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5ca9-104">Ignora uma linha inteira ao ler um fluxo de texto.</span><span class="sxs-lookup"><span data-stu-id="b5ca9-104">Skips one entire line when reading a text stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ca9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5ca9-105">Syntax</span></span>

<span data-ttu-id="b5ca9-106">*Stream*. SkipLine</span><span class="sxs-lookup"><span data-stu-id="b5ca9-106">*Stream*.SkipLine</span></span>

## <a name="remarks"></a><span data-ttu-id="b5ca9-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5ca9-107">Remarks</span></span>

<span data-ttu-id="b5ca9-p101">Todos os caracteres até e incluindo o próximo separador de próxima, serão ignorados. Por padrão, o [LineSeparator](lineseparator-property-ado.md) é **adCRLF**. Se você tentar ignorar além do [EOS](eos-property-ado.md), a posição atual simplesmente permanecerá no **EOS**.</span><span class="sxs-lookup"><span data-stu-id="b5ca9-p101">All characters up to, and including the next line separator, are skipped. By default, the [LineSeparator](lineseparator-property-ado.md) is **adCRLF**. If you attempt to skip past [EOS](eos-property-ado.md), the current position will simply remain at **EOS**.</span></span>

<span data-ttu-id="b5ca9-111">O método **SkipLine** é utilizado com fluxos de texto ([Type](type-property-ado-stream.md) é **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="b5ca9-111">The **SkipLine** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span>

