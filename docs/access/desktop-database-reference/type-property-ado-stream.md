---
title: Propriedade Type (Stream do ADO)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f1a5c9c69b5de6fbdf57efedf9724ae71ac151b7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945527"
---
# <a name="type-property-ado-stream"></a><span data-ttu-id="85bbb-102">Propriedade Type (Stream do ADO)</span><span class="sxs-lookup"><span data-stu-id="85bbb-102">Type property (ADO Stream)</span></span>


<span data-ttu-id="85bbb-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="85bbb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85bbb-104">Indica o tipo de dados contido no [Stream](stream-object-ado.md) (binário ou texto).</span><span class="sxs-lookup"><span data-stu-id="85bbb-104">Indicates the type of data contained in the [Stream](stream-object-ado.md) (binary or text).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="85bbb-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="85bbb-105">Settings and return values</span></span>

<span data-ttu-id="85bbb-p101">Define ou retorna um valor [StreamTypeEnum](streamtypeenum.md) que especifica o tipo de dados contido no objeto **Stream**. O valor padrão é **adTypeText**. Entretanto, se os dados binários forem inicialmente gravados em um **Stream** novo e vazio, a propriedade **Type** será alterada para **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="85bbb-p101">Sets or returns a [StreamTypeEnum](streamtypeenum.md) value that specifies the type of data contained in the **Stream** object. The default value is **adTypeText**. However, if binary data is initially written to a new, empty **Stream**, the **Type** will be changed to **adTypeBinary**.</span></span>

## <a name="remarks"></a><span data-ttu-id="85bbb-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="85bbb-109">Remarks</span></span>

<span data-ttu-id="85bbb-110">A propriedade **Type** será leitura/gravação somente quando a posição atual estiver no início do **Stream** ([Position](position-property-ado.md) for 0) e somente leitura em qualquer outra posição.</span><span class="sxs-lookup"><span data-stu-id="85bbb-110">The **Type** property is read/write only when the current position is at the beginning of the **Stream** ([Position](position-property-ado.md) is 0), and read-only at any other position.</span></span>

<span data-ttu-id="85bbb-p102">A propriedade **Type** determina quais métodos devem ser utilizados para a leitura e gravação do **Stream**. Para os **Streams** de texto, utilize [ReadText](readtext-method-ado.md) e [WriteText](writetext-method-ado.md). Para **Streams** binários, utilize [Read](read-method-ado.md) e [Write](write-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="85bbb-p102">The **Type** property determines which methods should be used for reading and writing the **Stream**. For text **Streams**, use [ReadText](readtext-method-ado.md) and [WriteText](writetext-method-ado.md). For binary **Streams**, use [Read](read-method-ado.md) and [Write](write-method-ado.md).</span></span>

