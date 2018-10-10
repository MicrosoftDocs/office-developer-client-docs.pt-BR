---
title: Propriedade Number (ADO)
TOCTitle: Number Property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4e9b048643b1892197f610ef6d53e6ba46b170d8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461960"
---
# <a name="number-property-ado"></a><span data-ttu-id="88765-102">Propriedade Number (ADO)</span><span class="sxs-lookup"><span data-stu-id="88765-102">Number Property (ADO)</span></span>


<span data-ttu-id="88765-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="88765-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="88765-104">Indica o número que identifica exclusivamente um objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="88765-104">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="88765-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="88765-105">Return Value</span></span>

<span data-ttu-id="88765-106">Retorna um valor **Long** que pode corresponder a uma das constantes [ErrorValueEnum](errorvalueenum.md).</span><span class="sxs-lookup"><span data-stu-id="88765-106">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="88765-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="88765-107">Remarks</span></span>

<span data-ttu-id="88765-p101">Use a propriedade **Number** para determinar qual erro ocorreu. O valor da propriedade é um número exclusivo que corresponde à condição de erro.</span><span class="sxs-lookup"><span data-stu-id="88765-p101">Use the **Number** property to determine which error occurred. The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="88765-110">A coleção [Errors](errors-collection-ado.md) retorna um HRESULT no formato hexadecimal (por exemplo, 0x80004005) ou valor extenso (por exemplo, 2147467259).</span><span class="sxs-lookup"><span data-stu-id="88765-110">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="88765-111">Esses HRESULTs podem ser causados por componentes de base, como o OLE DB ou o próprio OLE.</span><span class="sxs-lookup"><span data-stu-id="88765-111">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="88765-112">Para obter mais informações sobre esses números, consulte o capítulo 16 do *referência do programador DB OLE.*</span><span class="sxs-lookup"><span data-stu-id="88765-112">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

