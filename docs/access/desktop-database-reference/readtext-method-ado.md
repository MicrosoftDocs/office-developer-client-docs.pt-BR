---
title: Método ReadText (ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66db24f95e3f6338174be3a70ca75dbb3332adeb
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949387"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="7006b-102">Método ReadText (ADO)</span><span class="sxs-lookup"><span data-stu-id="7006b-102">ReadText method (ADO)</span></span>

<span data-ttu-id="7006b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7006b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7006b-104">Lê o número de caracteres especificado de um objeto [Stream](stream-object-ado.md) de texto.</span><span class="sxs-lookup"><span data-stu-id="7006b-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7006b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7006b-105">Syntax</span></span>

<span data-ttu-id="7006b-106">*Cadeia de caracteres* = *Stream*. ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="7006b-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="7006b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7006b-107">Parameters</span></span>

|<span data-ttu-id="7006b-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7006b-108">Parameter</span></span>|<span data-ttu-id="7006b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7006b-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7006b-110">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="7006b-110">*NumChars*</span></span> |<span data-ttu-id="7006b-p101">Opcional. Um valor **Long** que especifica o número de caracteres a serem lidos do arquivo ou um valor [StreamReadEnum](streamreadenum.md). O valor padrão é **adReadAll**.</span><span class="sxs-lookup"><span data-stu-id="7006b-p101">Optional. A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value. The default value is **adReadAll**.</span></span>|

## <a name="return-value"></a><span data-ttu-id="7006b-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7006b-114">Return value</span></span>

<span data-ttu-id="7006b-115">O método **ReadText** lê um número de caracteres especificado, uma linha inteira ou o fluxo inteiro a partir de um objeto **Stream** e retorna a sequência resultante.</span><span class="sxs-lookup"><span data-stu-id="7006b-115">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="7006b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7006b-116">Remarks</span></span>

<span data-ttu-id="7006b-p102">Se *NumChar* for maior que o número de caracteres restantes no fluxo, apenas os caracteres remanescentes serão retornados. A sequência lida não será enchida para corresponder ao comprimento especificado por *NumChar*. Se não houver caracteres restantes a ler, uma variante cujo valor é nulo será retornada. **ReadText** não pode ser utilizado para ler de trás para frente.</span><span class="sxs-lookup"><span data-stu-id="7006b-p102">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned. The string read is not padded to match the length specified by *NumChar*. If there are no characters left to read, a variant whose value is null is returned. **ReadText** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="7006b-p103">O método **ReadText** é utilizado com fluxos de texto ([Type](type-property-ado-stream.md) é **adTypeText**). Para fluxos binários (**Type** é **adTypeBinary**), utilize [Read](read-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7006b-p103">The **ReadText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**). For binary streams (**Type** is **adTypeBinary**), use [Read](read-method-ado.md).</span></span>

