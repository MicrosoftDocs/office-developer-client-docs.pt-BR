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
# <a name="lineseparator-property-ado"></a><span data-ttu-id="62e54-102">Propriedade LineSeparator (ADO)</span><span class="sxs-lookup"><span data-stu-id="62e54-102">LineSeparator Property (ADO)</span></span>


<span data-ttu-id="62e54-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="62e54-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="62e54-104">Indica o caractere binário a ser usado como o separador de linha nos objetos [Stream](stream-object-ado.md) de texto.</span><span class="sxs-lookup"><span data-stu-id="62e54-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="62e54-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="62e54-105">Settings and Return Values</span></span>

<span data-ttu-id="62e54-p101">Define ou retorna um valor [LineSeparatorsEnum](lineseparatorsenum.md) que indica o caractere do separador de linha usado no **Stream**. O valor padrão é **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="62e54-p101">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**. The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="62e54-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="62e54-108">Remarks</span></span>

<span data-ttu-id="62e54-p102">**LineSeparator** é usada para interpretar as linhas ao ler o conteúdo de um **Stream** de texto. As linhas podem ser ignoradas com o método [SkipLine](skipline-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="62e54-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="62e54-p103">**LineSeparator** é usada apenas com objetos **Stream** de texto ([Type](type-property-ado-stream.md) é **adTypeText**). Esta propriedade será ignorada se **Type** for **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="62e54-p103">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>

