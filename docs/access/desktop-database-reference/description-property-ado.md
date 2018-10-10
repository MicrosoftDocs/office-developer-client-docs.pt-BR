---
title: Propriedade Description (ADO)
TOCTitle: Description Property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3837d60b58772bbe6b65af6673c4eaa471507e66
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462733"
---
# <a name="description-property-ado"></a><span data-ttu-id="657c8-102">Propriedade Description (ADO)</span><span class="sxs-lookup"><span data-stu-id="657c8-102">Description Property (ADO)</span></span>


<span data-ttu-id="657c8-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="657c8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="657c8-104">Descreve um objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="657c8-104">Describes an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="657c8-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="657c8-105">Return Value</span></span>

<span data-ttu-id="657c8-106">Retorna um valor **String** contendo uma descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="657c8-106">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="657c8-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="657c8-107">Remarks</span></span>

<span data-ttu-id="657c8-p101">Use a propriedade **Description** para obter uma breve descrição do erro. Exiba essa propriedade para alertar o usuário sobre um erro que você não pode ou não deseja resolver. A sequência virá do ADO ou de um provedor.</span><span class="sxs-lookup"><span data-stu-id="657c8-p101">Use the **Description** property to obtain a short description of the error. Display this property to alert the user to an error that you cannot or do not want to handle. The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="657c8-p102">Os provedores são responsáveis por passar textos de erro específicos para o ADO. O ADO adiciona um objeto [Error](error-object-ado.md) à coleção **Errors** a cada erro de provedor ou alerta que recebe. Enumere a coleção **Errors** para rastrear os erros que são passados pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="657c8-p102">Providers are responsible for passing specific error text to ADO. ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives. Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

