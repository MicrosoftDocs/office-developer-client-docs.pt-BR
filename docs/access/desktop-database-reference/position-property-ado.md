---
title: Propriedade Position (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d4d907cedc3490f4ca13d47a12b9719cf3e2ee1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997151"
---
# <a name="position-property-ado"></a><span data-ttu-id="84b66-102">Propriedade Position (ADO)</span><span class="sxs-lookup"><span data-stu-id="84b66-102">Position property (ADO)</span></span>

<span data-ttu-id="84b66-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="84b66-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="84b66-104">Indica a posição atual em um objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="84b66-104">Indicates the current position within a [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="84b66-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="84b66-105">Settings and return values</span></span>

<span data-ttu-id="84b66-p101">Define ou retorna um valor **Long** que especifica o deslocamento, em número de bytes, da posição atual a partir do início do fluxo. O padrão é 0, que representa o primeiro byte no fluxo.</span><span class="sxs-lookup"><span data-stu-id="84b66-p101">Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream. The default is 0, which represents the first byte in the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="84b66-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="84b66-108">Remarks</span></span>

<span data-ttu-id="84b66-p102">A posição atual pode ser movida para um ponto posterior ao final do fluxo. Se você especificar a posição atual além do final do fluxo, o [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) do objeto **Stream** aumentará de forma adequada. Os bytes novos adicionados desta forma serão nulos.</span><span class="sxs-lookup"><span data-stu-id="84b66-p102">The current position can be moved to a point after the end of the stream. If you specify the current position beyond the end of the stream, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** object will be increased accordingly. Any new bytes added in this way will be null.</span></span>

> [!NOTE]
> <span data-ttu-id="84b66-p103">[!OBSERVAçãO] **Position** sempre mede bytes. Para fluxos de texto que utilizam conjuntos de caracteres com vários bytes, multiplique a posição pelo tamanho do caractere para determinar o número do caractere. Por exemplo, para um conjunto de caracteres de dois bytes, o primeiro caractere estará na posição 0, o segundo caractere na posição 2, o terceiro na posição 4, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="84b66-p103">**Position** always measures bytes. For text streams using multibyte character sets, multiply the position by the character size to determine the character number. For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</span></span>

<span data-ttu-id="84b66-p104">Os valores negativos não podem ser utilizados para alterar a posição atual em um **Stream**. Somente números positivos podem ser utilizados para **Position**.</span><span class="sxs-lookup"><span data-stu-id="84b66-p104">Negative values cannot be used to change the current position in a **Stream**. Only positive numbers can be used for **Position**.</span></span>

<span data-ttu-id="84b66-p105">Para objetos **Stream** somente leitura, o ADO não retornará um erro se **Position** for definida com um valor superior ao **Size** do **Stream**. Isto não altera o tamanho do **Stream** nem do conteúdo do **Stream**. Entretanto, esse procedimento deve ser evitado, pois resulta em um valor **Position** insignificante.</span><span class="sxs-lookup"><span data-stu-id="84b66-p105">For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**. This does not change the size of the **Stream**, or alter the **Stream** contents in any way. However, doing this should be avoided because it results in a meaningless **Position** value.</span></span>

