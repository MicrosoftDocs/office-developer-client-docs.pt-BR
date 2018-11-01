---
title: Liberar o método - ActiveX Data Objects (ADO)
TOCTitle: Flush Method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ecf56ccf715df324798cd9b5adfc57f92591f05
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885126"
---
# <a name="flush-method-ado"></a><span data-ttu-id="d4688-102">Método Flush (ADO)</span><span class="sxs-lookup"><span data-stu-id="d4688-102">Flush Method (ADO)</span></span>


<span data-ttu-id="d4688-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d4688-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d4688-104">Força que o com que o conteúdo do [Stream](stream-object-ado.md) remanescente no buffer do ADO vá para o objeto base com o qual o **Stream** está associado.</span><span class="sxs-lookup"><span data-stu-id="d4688-104">Forces the contents of the [Stream](stream-object-ado.md) remaining in the ADO buffer to the underlying object with which the **Stream** is associated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4688-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4688-105">Syntax</span></span>

<span data-ttu-id="d4688-106">*Stream*. Liberar</span><span class="sxs-lookup"><span data-stu-id="d4688-106">*Stream*.Flush</span></span>

## <a name="remarks"></a><span data-ttu-id="d4688-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4688-107">Remarks</span></span>

<span data-ttu-id="d4688-p101">Este método pode ser utilizado para enviar o conteúdo do buffer do fluxo para o objeto base (por exemplo, o nó ou arquivo representado pela URL que é a fonte do objeto **Stream** ). Este método deve ser chamado quando você deseja assegurar que todas as alterações feitas no conteúdo de um **Stream** sejam gravadas. No entanto, com o ADO, geralmente não é necessário chamar **Flush**, pois o ADO esvazia continuamente seu buffer o tanto quanto possível em segundo plano. As alterações no conteúdo de um **Stream** são feitas automaticamente, não armazenadas em cache até que **Flush** seja chamado.</span><span class="sxs-lookup"><span data-stu-id="d4688-p101">This method may be used to send the contents of the stream buffer to the underlying object (for example, the node or file represented by the URL that is the source of the **Stream** object). This method should be called when you want to ensure that all changes made to the contents of a **Stream** have been written. However, with ADO it is not usually necessary to call **Flush**, as ADO continuously flushes its buffer as much as possible in the background. Changes to the content of a **Stream** are made automatically, not cached until **Flush** is called.</span></span>

<span data-ttu-id="d4688-112">Fechar um **Stream** com o método [Close](close-method-ado.md) esvazia automaticamente o conteúdo de um **Stream**; não há necessidade em chamar explicitamente **Flush** imediatamente antes de **Close**.</span><span class="sxs-lookup"><span data-stu-id="d4688-112">Closing a **Stream** with the [Close](close-method-ado.md) method flushes the contents of a **Stream** automatically; there is no need to explicitly call **Flush** immediately before **Close**.</span></span>

