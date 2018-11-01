---
title: Método ReadText (ADO)
TOCTitle: ReadText Method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e4bc9febb76f71068517d2d83cddbdf4edee53b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891132"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="7a2d0-102">Método ReadText (ADO)</span><span class="sxs-lookup"><span data-stu-id="7a2d0-102">ReadText Method (ADO)</span></span>


<span data-ttu-id="7a2d0-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a2d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a2d0-104">Lê o número de caracteres especificado de um objeto [Stream](stream-object-ado.md) de texto.</span><span class="sxs-lookup"><span data-stu-id="7a2d0-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a2d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a2d0-105">Syntax</span></span>

<span data-ttu-id="7a2d0-106">*Cadeia de caracteres* = *Stream*. ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="7a2d0-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="7a2d0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a2d0-107">Parameters</span></span>

  - <span data-ttu-id="7a2d0-108">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="7a2d0-108">*NumChars*</span></span>

  - <span data-ttu-id="7a2d0-p101">Opcional. Um valor **Long** que especifica o número de caracteres a serem lidos do arquivo ou um valor [StreamReadEnum](streamreadenum.md). O valor padrão é **adReadAll**.</span><span class="sxs-lookup"><span data-stu-id="7a2d0-p101">Optional. A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value. The default value is **adReadAll**.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a2d0-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7a2d0-112">Return value</span></span>

<span data-ttu-id="7a2d0-113">O método **ReadText** lê um número de caracteres especificado, uma linha inteira ou o fluxo inteiro a partir de um objeto **Stream** e retorna a sequência resultante.</span><span class="sxs-lookup"><span data-stu-id="7a2d0-113">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a2d0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a2d0-114">Remarks</span></span>

<span data-ttu-id="7a2d0-p102">Se *NumChar* for maior que o número de caracteres restantes no fluxo, apenas os caracteres remanescentes serão retornados. A sequência lida não será enchida para corresponder ao comprimento especificado por *NumChar*. Se não houver caracteres restantes a ler, uma variante cujo valor é nulo será retornada. **ReadText** não pode ser utilizado para ler de trás para frente.</span><span class="sxs-lookup"><span data-stu-id="7a2d0-p102">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned. The string read is not padded to match the length specified by *NumChar*. If there are no characters left to read, a variant whose value is null is returned. **ReadText** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7a2d0-p103">O método <STRONG>ReadText</STRONG> é utilizado com fluxos de texto (<A href="type-property-ado-stream.md">Type</A> é <STRONG>adTypeText</STRONG>). Para fluxos binários (<STRONG>Type</STRONG> é <STRONG>adTypeBinary</STRONG>), utilize <A href="read-method-ado.md">Read</A>.</span><span class="sxs-lookup"><span data-stu-id="7a2d0-p103">The <STRONG>ReadText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>). For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="read-method-ado.md">Read</A>.</span></span></P>


