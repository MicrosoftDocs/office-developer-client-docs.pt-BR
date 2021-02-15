---
title: Propriedade LineSeparator (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e941339ad1c8622d1c87ada848a44fa82a9ef2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289946"
---
# <a name="lineseparator-property-ado"></a><span data-ttu-id="a02a9-102">Propriedade LineSeparator (ADO)</span><span class="sxs-lookup"><span data-stu-id="a02a9-102">LineSeparator property (ADO)</span></span>


<span data-ttu-id="a02a9-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a02a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a02a9-104">Indica o caractere binário a ser usado como o separador de linha nos objetos [Stream](stream-object-ado.md) de texto.</span><span class="sxs-lookup"><span data-stu-id="a02a9-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a02a9-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="a02a9-105">Settings and return values</span></span>

<span data-ttu-id="a02a9-106">Define ou retorna um valor [LineSeparatorsEnum](lineseparatorsenum.md) que indica o caractere do separador de linha usado no **Stream**.</span><span class="sxs-lookup"><span data-stu-id="a02a9-106">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**.</span></span> <span data-ttu-id="a02a9-107">O valor padrão é **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="a02a9-107">The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a02a9-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a02a9-108">Remarks</span></span>

<span data-ttu-id="a02a9-p102">**LineSeparator** é usada para interpretar as linhas ao ler o conteúdo de um **Stream** de texto. As linhas podem ser ignoradas com o método [SkipLine](skipline-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a02a9-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="a02a9-111">**LineSeparator** é usada apenas com objetos **Stream** de texto ([Type](type-property-ado-stream.md) é **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="a02a9-111">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="a02a9-112">Esta propriedade será ignorada se **Type** for **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="a02a9-112">This property is ignored if **Type** is **adTypeBinary**.</span></span>

