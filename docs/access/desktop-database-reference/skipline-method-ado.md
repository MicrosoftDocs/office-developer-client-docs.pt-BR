---
title: Método SkipLine (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d22aca01c468813f280472281719822a7d884988
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923921"
---
# <a name="skipline-method-ado"></a><span data-ttu-id="7ff34-102">Método SkipLine (ADO)</span><span class="sxs-lookup"><span data-stu-id="7ff34-102">SkipLine method (ADO)</span></span>


<span data-ttu-id="7ff34-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ff34-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ff34-104">Ignora uma linha inteira ao ler um fluxo de texto.</span><span class="sxs-lookup"><span data-stu-id="7ff34-104">Skips one entire line when reading a text stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff34-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ff34-105">Syntax</span></span>

<span data-ttu-id="7ff34-106">*Stream*. SkipLine</span><span class="sxs-lookup"><span data-stu-id="7ff34-106">*Stream*.SkipLine</span></span>

## <a name="remarks"></a><span data-ttu-id="7ff34-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ff34-107">Remarks</span></span>

<span data-ttu-id="7ff34-p101">Todos os caracteres até e incluindo o próximo separador de próxima, serão ignorados. Por padrão, o [LineSeparator](lineseparator-property-ado.md) é **adCRLF**. Se você tentar ignorar além do [EOS](eos-property-ado.md), a posição atual simplesmente permanecerá no **EOS**.</span><span class="sxs-lookup"><span data-stu-id="7ff34-p101">All characters up to, and including the next line separator, are skipped. By default, the [LineSeparator](lineseparator-property-ado.md) is **adCRLF**. If you attempt to skip past [EOS](eos-property-ado.md), the current position will simply remain at **EOS**.</span></span>

<span data-ttu-id="7ff34-111">O método **SkipLine** é utilizado com fluxos de texto ([Type](type-property-ado-stream.md) é **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="7ff34-111">The **SkipLine** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span>

