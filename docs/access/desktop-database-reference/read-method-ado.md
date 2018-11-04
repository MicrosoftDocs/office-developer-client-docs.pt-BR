---
title: Leia o método - ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bcee0de272a14825f978abb1f6dd2834a998f86
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949331"
---
# <a name="read-method-ado"></a><span data-ttu-id="a9b79-102">Método Read (ADO)</span><span class="sxs-lookup"><span data-stu-id="a9b79-102">Read method (ADO)</span></span>

<span data-ttu-id="a9b79-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9b79-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9b79-104">Lê um número de bytes especificado de um objeto [Stream](stream-object-ado.md) binário.</span><span class="sxs-lookup"><span data-stu-id="a9b79-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9b79-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9b79-105">Syntax</span></span>

<span data-ttu-id="a9b79-106">*Variant* = *Stream*. Leitura (*NumBytes* )</span><span class="sxs-lookup"><span data-stu-id="a9b79-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="a9b79-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9b79-107">Parameters</span></span>

|<span data-ttu-id="a9b79-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9b79-108">Parameter</span></span>|<span data-ttu-id="a9b79-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9b79-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a9b79-110">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="a9b79-110">*NumBytes*</span></span> |<span data-ttu-id="a9b79-p101">Opcional. Um valor **Long** que especifica o número de bytes a serem lidos do arquivo ou o valor [adReadAll](streamreadenum.md) de **StreamReadEnum**, que é o padrão.</span><span class="sxs-lookup"><span data-stu-id="a9b79-p101">Optional. A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>|

## <a name="return-value"></a><span data-ttu-id="a9b79-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a9b79-113">Return value</span></span>

<span data-ttu-id="a9b79-114">O método **Read** lê um número de bytes especificado ou o fluxo inteiro de um objeto **Stream** e retorna os dados resultantes como uma **Variant**.</span><span class="sxs-lookup"><span data-stu-id="a9b79-114">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9b79-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9b79-115">Remarks</span></span>

<span data-ttu-id="a9b79-p102">Se *NumBytes* for maior que o número de bytes restantes no **Stream**, apenas os bytes remanescentes serão retornados. Os dados lidos não serão enchidos para corresponder ao comprimento especificado por *NumBytes*. Se não houver bytes restantes a ler, uma variante com um valor nulo será retornada. **Read** não pode ser utilizado para ler de trás para frente.</span><span class="sxs-lookup"><span data-stu-id="a9b79-p102">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned. The data read is not padded to match the length specified by *NumBytes*. If there are no bytes left to read, a variant with a null value is returned. **Read** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="a9b79-p103">*NumBytes* sempre mede bytes. Para objetos **Stream** de texto ([Type](type-property-ado-stream.md) é **adTypeText**), utilize [ReadText](readtext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a9b79-p103">*NumBytes* always measures bytes. For text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**), use [ReadText](readtext-method-ado.md).</span></span>


