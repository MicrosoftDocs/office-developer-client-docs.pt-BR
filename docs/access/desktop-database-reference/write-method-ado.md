---
title: Escrever o método - ActiveX Data Objects (ADO)
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5987b16c033b13be145e60317cdfdc821851be38
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867409"
---
# <a name="write-method-ado"></a><span data-ttu-id="ca8fd-102">Método Write (ADO)</span><span class="sxs-lookup"><span data-stu-id="ca8fd-102">Write Method (ADO)</span></span>


<span data-ttu-id="ca8fd-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca8fd-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ca8fd-104">Grava dados binários em um objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ca8fd-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca8fd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca8fd-105">Syntax</span></span>

<span data-ttu-id="ca8fd-106">*Stream*. Gravar*Buffer*</span><span class="sxs-lookup"><span data-stu-id="ca8fd-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="ca8fd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca8fd-107">Parameters</span></span>

  - <span data-ttu-id="ca8fd-108">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="ca8fd-108">*Buffer*</span></span>

  - <span data-ttu-id="ca8fd-109">Uma **Variant** que contém uma matriz de bytes a serem gravados.</span><span class="sxs-lookup"><span data-stu-id="ca8fd-109">A **Variant** that contains an array of bytes to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca8fd-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca8fd-110">Remarks</span></span>

<span data-ttu-id="ca8fd-111">Os bytes especificados são gravados no objeto **Stream** sem nenhum espaço intermediário entre cada byte.</span><span class="sxs-lookup"><span data-stu-id="ca8fd-111">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="ca8fd-p101">A [Position](position-property-ado.md) atual será definida para o byte que segue os dados gravados. O método **Write** não trunca o restante dos dados em um fluxo. Se você deseja truncar esses bytes, chame [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ca8fd-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="ca8fd-115">Se você gravar após a posição [EOS](eos-property-ado.md) atual, o [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de **Stream** será incrementado para conter quaisquer bytes novos e **EOS** será movido para o último novo byte em **Stream**.</span><span class="sxs-lookup"><span data-stu-id="ca8fd-115">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ca8fd-p102">O método <STRONG>Write</STRONG> é utilizado com fluxos binários (<A href="type-property-ado-stream.md">Type</A> é <STRONG>adTypeBinary</STRONG>). Para fluxos de texto (<STRONG>Type</STRONG> é <STRONG>adTypeText</STRONG>), utilize <A href="writetext-method-ado.md">WriteText</A>.</span><span class="sxs-lookup"><span data-stu-id="ca8fd-p102">The <STRONG>Write</STRONG> method is used with binary streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeBinary</STRONG>). For text streams (<STRONG>Type</STRONG> is <STRONG>adTypeText</STRONG>), use <A href="writetext-method-ado.md">WriteText</A>.</span></span></P>


