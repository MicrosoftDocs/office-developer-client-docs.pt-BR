---
title: Método WriteText (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c0c4668141c0da6e5faddee009d2548f1ee2c53
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926994"
---
# <a name="writetext-method-ado"></a><span data-ttu-id="d7f16-102">Método WriteText (ADO)</span><span class="sxs-lookup"><span data-stu-id="d7f16-102">WriteText method (ADO)</span></span>


<span data-ttu-id="d7f16-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7f16-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7f16-104">Grava uma sequência de texto especificada em um objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d7f16-104">Writes a specified text string to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f16-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7f16-105">Syntax</span></span>

<span data-ttu-id="d7f16-106">*Stream*. WriteText*dados*, *Opções*</span><span class="sxs-lookup"><span data-stu-id="d7f16-106">*Stream*.WriteText*Data*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="d7f16-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7f16-107">Parameters</span></span>

  - <span data-ttu-id="d7f16-108">*Data*</span><span class="sxs-lookup"><span data-stu-id="d7f16-108">*Data*</span></span>

  - <span data-ttu-id="d7f16-109">Um valor **String** que contém o texto em caracteres a ser gravado.</span><span class="sxs-lookup"><span data-stu-id="d7f16-109">A **String** value that contains the text in characters to be written.</span></span>

  - <span data-ttu-id="d7f16-110">*Options*</span><span class="sxs-lookup"><span data-stu-id="d7f16-110">*Options*</span></span>

  - <span data-ttu-id="d7f16-p101">Opcional. Um valor [StreamWriteEnum](streamwriteenum.md) que especifica se um caractere separador de linha deve ser gravado no final da sequência especificada.</span><span class="sxs-lookup"><span data-stu-id="d7f16-p101">Optional. A [StreamWriteEnum](streamwriteenum.md) value that specifies whether a line separator character must be written at the end of the specified string.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7f16-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7f16-113">Remarks</span></span>

<span data-ttu-id="d7f16-114">As sequências especificadas são gravadas no objeto **Stream** sem nenhum espaço ou caractere intermediário entre cada sequência.</span><span class="sxs-lookup"><span data-stu-id="d7f16-114">Specified strings are written to the **Stream** object without any intervening spaces or characters between each string.</span></span>

<span data-ttu-id="d7f16-p102">A [Position](position-property-ado.md) atual será definida para o caractere que segue os dados gravados. O método **WriteText** não trunca o restante dos dados em um fluxo. Se você deseja truncar esses caracteres, chame [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d7f16-p102">The current [Position](position-property-ado.md) is set to the character following the written data. The **WriteText** method does not truncate the rest of the data in a stream. If you want to truncate these characters, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="d7f16-118">Se você gravar após a posição [EOS](eos-property-ado.md) atual, o [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de **Stream** será incrementado para conter quaisquer caracteres novos e **EOS** será movido para o último novo byte em **Stream**.</span><span class="sxs-lookup"><span data-stu-id="d7f16-118">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new characters, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d7f16-p103">O método <STRONG>WriteText</STRONG> é utilizado com fluxos de texto (<A href="type-property-ado-stream.md">Type</A> é <STRONG>adTypeText</STRONG>). Para fluxos binários (<STRONG>Type</STRONG> é <STRONG>adTypeBinary</STRONG>), utilize <A href="write-method-ado.md">Write</A>.</span><span class="sxs-lookup"><span data-stu-id="d7f16-p103">The <STRONG>WriteText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>). For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="write-method-ado.md">Write</A>.</span></span></P>


