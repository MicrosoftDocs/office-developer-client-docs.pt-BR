---
title: Leia o método - ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6de4ea8a8dd64ff4c0562111f6e42ed089754f3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919455"
---
# <a name="read-method-ado"></a><span data-ttu-id="9f525-102">Método Read (ADO)</span><span class="sxs-lookup"><span data-stu-id="9f525-102">Read method (ADO)</span></span>


<span data-ttu-id="9f525-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f525-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f525-104">Lê um número de bytes especificado de um objeto [Stream](stream-object-ado.md) binário.</span><span class="sxs-lookup"><span data-stu-id="9f525-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f525-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f525-105">Syntax</span></span>

<span data-ttu-id="9f525-106">*Variant* = *Stream*. Leitura (*NumBytes* )</span><span class="sxs-lookup"><span data-stu-id="9f525-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="9f525-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f525-107">Parameters</span></span>

  - <span data-ttu-id="9f525-108">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="9f525-108">*NumBytes*</span></span>

  - <span data-ttu-id="9f525-p101">Opcional. Um valor **Long** que especifica o número de bytes a serem lidos do arquivo ou o valor [adReadAll](streamreadenum.md) de **StreamReadEnum**, que é o padrão.</span><span class="sxs-lookup"><span data-stu-id="9f525-p101">Optional. A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f525-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9f525-111">Return value</span></span>

<span data-ttu-id="9f525-112">O método **Read** lê um número de bytes especificado ou o fluxo inteiro de um objeto **Stream** e retorna os dados resultantes como uma **Variant**.</span><span class="sxs-lookup"><span data-stu-id="9f525-112">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f525-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f525-113">Remarks</span></span>

<span data-ttu-id="9f525-p102">Se *NumBytes* for maior que o número de bytes restantes no **Stream**, apenas os bytes remanescentes serão retornados. Os dados lidos não serão enchidos para corresponder ao comprimento especificado por *NumBytes*. Se não houver bytes restantes a ler, uma variante com um valor nulo será retornada. **Read** não pode ser utilizado para ler de trás para frente.</span><span class="sxs-lookup"><span data-stu-id="9f525-p102">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned. The data read is not padded to match the length specified by *NumBytes*. If there are no bytes left to read, a variant with a null value is returned. **Read** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9f525-p103"><EM>NumBytes</EM> sempre mede bytes. Para objetos <STRONG>Stream</STRONG> de texto (<A href="type-property-ado-stream.md">Type</A> é <STRONG>adTypeText</STRONG>), utilize <A href="readtext-method-ado.md">ReadText</A>.</span><span class="sxs-lookup"><span data-stu-id="9f525-p103"><EM>NumBytes</EM> always measures bytes. For text <STRONG>Stream</STRONG> objects (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>), use <A href="readtext-method-ado.md">ReadText</A>.</span></span></P>


