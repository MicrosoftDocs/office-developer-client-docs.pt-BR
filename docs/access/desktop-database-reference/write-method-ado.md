---
title: Escrever o método - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6f4bba55ec3a32d206d3a7bfd001e96cd94923e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702513"
---
# <a name="write-method-ado"></a><span data-ttu-id="f903e-102">Método Write (ADO)</span><span class="sxs-lookup"><span data-stu-id="f903e-102">Write method (ADO)</span></span>

<span data-ttu-id="f903e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f903e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f903e-104">Grava dados binários em um objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f903e-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f903e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f903e-105">Syntax</span></span>

<span data-ttu-id="f903e-106">*Stream*. Gravar*Buffer*</span><span class="sxs-lookup"><span data-stu-id="f903e-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="f903e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f903e-107">Parameters</span></span>

|<span data-ttu-id="f903e-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f903e-108">Parameter</span></span>|<span data-ttu-id="f903e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f903e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f903e-110">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="f903e-110">*Buffer*</span></span> |<span data-ttu-id="f903e-111">Uma **Variant** que contém uma matriz de bytes a serem gravados.</span><span class="sxs-lookup"><span data-stu-id="f903e-111">A **Variant** that contains an array of bytes to be written.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f903e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f903e-112">Remarks</span></span>

<span data-ttu-id="f903e-113">Os bytes especificados são gravados no objeto **Stream** sem nenhum espaço intermediário entre cada byte.</span><span class="sxs-lookup"><span data-stu-id="f903e-113">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="f903e-p101">A [Position](position-property-ado.md) atual será definida para o byte que segue os dados gravados. O método **Write** não trunca o restante dos dados em um fluxo. Se você deseja truncar esses bytes, chame [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f903e-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="f903e-117">Se você gravar após a posição [EOS](eos-property-ado.md) atual, o [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) de **Stream** será incrementado para conter quaisquer bytes novos e **EOS** será movido para o último novo byte em **Stream**.</span><span class="sxs-lookup"><span data-stu-id="f903e-117">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="f903e-p102">O método **Write** é utilizado com fluxos binários ([Type](type-property-ado-stream.md) é **adTypeBinary**). Para fluxos de texto (**Type** é **adTypeText**), utilize [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f903e-p102">The **Write** method is used with binary streams ([Type](type-property-ado-stream.md) is **adTypeBinary**). For text streams (**Type** is **adTypeText**), use [WriteText](writetext-method-ado.md).</span></span>

