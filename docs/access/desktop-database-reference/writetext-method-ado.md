---
title: Método WriteText (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92983163a909e72c3da142ebcf63b7e0723e96af
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726243"
---
# <a name="writetext-method-ado"></a><span data-ttu-id="1947f-102">Método WriteText (ADO)</span><span class="sxs-lookup"><span data-stu-id="1947f-102">WriteText method (ADO)</span></span>

<span data-ttu-id="1947f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1947f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1947f-104">Grava uma sequência de texto especificada em um objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1947f-104">Writes a specified text string to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1947f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1947f-105">Syntax</span></span>

<span data-ttu-id="1947f-106">*Stream*. WriteText*dados*, *Opções*</span><span class="sxs-lookup"><span data-stu-id="1947f-106">*Stream*.WriteText*Data*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="1947f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1947f-107">Parameters</span></span>

|<span data-ttu-id="1947f-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1947f-108">Parameter</span></span>|<span data-ttu-id="1947f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1947f-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1947f-110">*Dados*</span><span class="sxs-lookup"><span data-stu-id="1947f-110">*Data*</span></span> |<span data-ttu-id="1947f-111">Um valor **String** que contém o texto em caracteres a ser gravado.</span><span class="sxs-lookup"><span data-stu-id="1947f-111">A **String** value that contains the text in characters to be written.</span></span>|
|<span data-ttu-id="1947f-112">*Options*</span><span class="sxs-lookup"><span data-stu-id="1947f-112">*Options*</span></span> |<span data-ttu-id="1947f-p101">Opcional. Um valor [StreamWriteEnum](streamwriteenum.md) que especifica se um caractere separador de linha deve ser gravado no final da sequência especificada.</span><span class="sxs-lookup"><span data-stu-id="1947f-p101">Optional. A [StreamWriteEnum](streamwriteenum.md) value that specifies whether a line separator character must be written at the end of the specified string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1947f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1947f-115">Remarks</span></span>

<span data-ttu-id="1947f-116">As sequências especificadas são gravadas no objeto **Stream** sem nenhum espaço ou caractere intermediário entre cada sequência.</span><span class="sxs-lookup"><span data-stu-id="1947f-116">Specified strings are written to the **Stream** object without any intervening spaces or characters between each string.</span></span>

<span data-ttu-id="1947f-p102">A [Position](position-property-ado.md) atual será definida para o caractere que segue os dados gravados. O método **WriteText** não trunca o restante dos dados em um fluxo. Se você deseja truncar esses caracteres, chame [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1947f-p102">The current [Position](position-property-ado.md) is set to the character following the written data. The **WriteText** method does not truncate the rest of the data in a stream. If you want to truncate these characters, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="1947f-120">Se você gravar após a posição [EOS](eos-property-ado.md) atual, o [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) de **Stream** será incrementado para conter quaisquer caracteres novos e **EOS** será movido para o último novo byte em **Stream**.</span><span class="sxs-lookup"><span data-stu-id="1947f-120">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** will be increased to contain any new characters, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="1947f-p103">O método **WriteText** é utilizado com fluxos de texto ([Type](type-property-ado-stream.md) é **adTypeText**). Para fluxos binários (**Type** é **adTypeBinary**), utilize [Write](write-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1947f-p103">The **WriteText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**). For binary streams (**Type** is **adTypeBinary**), use [Write](write-method-ado.md).</span></span>


