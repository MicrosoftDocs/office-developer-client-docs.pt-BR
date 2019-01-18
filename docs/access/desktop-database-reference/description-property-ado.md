---
title: Propriedade Description (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba6d05aa1bfb626520af60a30279983bae6fa566
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698929"
---
# <a name="description-property-ado"></a><span data-ttu-id="6bc0c-102">Propriedade Description (ADO)</span><span class="sxs-lookup"><span data-stu-id="6bc0c-102">Description property (ADO)</span></span>


<span data-ttu-id="6bc0c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6bc0c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6bc0c-104">Descreve um objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6bc0c-104">Describes an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="6bc0c-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6bc0c-105">Return value</span></span>

<span data-ttu-id="6bc0c-106">Retorna um valor **String** contendo uma descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="6bc0c-106">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bc0c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bc0c-107">Remarks</span></span>

<span data-ttu-id="6bc0c-p101">Use a propriedade **Description** para obter uma breve descrição do erro. Exiba essa propriedade para alertar o usuário sobre um erro que você não pode ou não deseja resolver. A sequência virá do ADO ou de um provedor.</span><span class="sxs-lookup"><span data-stu-id="6bc0c-p101">Use the **Description** property to obtain a short description of the error. Display this property to alert the user to an error that you cannot or do not want to handle. The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="6bc0c-p102">Os provedores são responsáveis por passar textos de erro específicos para o ADO. O ADO adiciona um objeto [Error](error-object-ado.md) à coleção **Errors** a cada erro de provedor ou alerta que recebe. Enumere a coleção **Errors** para rastrear os erros que são passados pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="6bc0c-p102">Providers are responsible for passing specific error text to ADO. ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives. Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

